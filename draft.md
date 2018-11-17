Draft
================
Final Project
11/17/2018

Importing data

``` r
load("./data/Wave 1/DS0001/34315-0001-Data.rda")
load("./data/Wave 2/DS0001/37105-0001-Data.rda")
load("./data/Wave 3/DS0001/37106-0001-Data.rda")

wave_1_data = da34315.0001
wave_2_data = da37105.0001
wave_3_data = da37106.0001
```

Creating Graphs

``` r
countplot = wave_3_data %>% 
  select(PH001, PH002, SEX) %>% 
  mutate(physical = case_when(
    PH001 == "(01) Excellent" ~ "Excellent", 
    PH001 == "(02) Very Good" ~ "Very Good",
    PH001 == "(03) Good" ~ "Good", 
    PH001 == "(04) Fair" ~ "Fair", 
    PH001 == "(05) Poor" ~ "Poor"), 
    
  mental = case_when(
    PH002 == "(01) Excellent" ~ "Excellent", 
    PH002 == "(02) Very Good" ~ "Very Good",
    PH002 == "(03) Good" ~ "Good", 
    PH002 == "(04) Fair" ~ "Fair", 
    PH002 == "(05) Poor" ~ "Poor"),
  
  sex = case_when(
    SEX == "(1) Male" ~ "Male",
    SEX == "(2) Female" ~ "Female"
  ),
  
  physical = factor(physical, levels = c("Excellent", "Very Good", "Good", "Fair", "Poor")), 
  
  mental = factor(mental, levels = c("Excellent", "Very Good", "Good", "Fair", "Poor"))
        ) %>% 
  select(-PH001, -PH002, -SEX)

countplot %>%
  ggplot(aes(x = physical, y = mental, color = ..n..)) +
  geom_count(alpha = 0.8) +
  labs(
    x = "Self-Rated Physical Health",
    y = "Self-Rated Mental Health"
  ) +
  facet_grid(~sex) +
  theme_bw() +
  theme(legend.position = "none")
```

![](draft_files/figure-markdown_github/countplot-1.png)

``` r
wave_1_data = wave_1_data %>% 
  mutate(MHUCLA_LONELINESS_1 = MHUCLA_LONELINESS)

wave_2_data = wave_2_data %>% 
  mutate(MHUCLA_LONELINESS_2 = MHUCLA_LONELINESS)

wave_3_data = wave_3_data %>% 
  mutate(MHUCLA_LONELINESS_3 = MHUCLA_LONELINESS)

spaghetti = 
  merge(wave_1_data, wave_2_data, by = "ID") %>% 
  merge(wave_3_data, by = "ID") %>% 

  select(ID, SEX.x, CS006, MHUCLA_LONELINESS_1, MHUCLA_LONELINESS_2, MHUCLA_LONELINESS_3) %>% 
  arrange(ID) %>% 
  mutate(sex = case_when(
    SEX.x == "(1) Male" ~ "Male",
    SEX.x == "(2) Female" ~ "Female"
  ),
    marital_status = case_when(
      CS006 == "(1) Married" ~ "Married",
      CS006 == "(2) Living with a partner as if married" ~ "Cohabitation",
      CS006 == "(3) Single(never married)" ~ "Single",
      CS006 == "(4) Separated" ~ "Separated",
      CS006 == "(5) Divorced" ~ "Divorced",
      CS006 == "(6) Widowed" ~ "Widowed"
)) %>% 
  filter(marital_status == "Widowed") %>% 
  select(-SEX.x, -CS006) %>% 
  gather(key = wave, value = loneliness_value, MHUCLA_LONELINESS_1:MHUCLA_LONELINESS_3) %>% 
  mutate(wave = case_when(
      wave == "MHUCLA_LONELINESS_1" ~ 1, 
      wave == "MHUCLA_LONELINESS_2" ~ 2, 
      wave == "MHUCLA_LONELINESS_3" ~ 3
  )) %>% 
  janitor::clean_names()

spaghetti %>% 
  filter(sex == "Male", loneliness_value != "NA") %>% 
  ggplot(aes(x = wave, y = loneliness_value, color = id)) +
  geom_line() +
  theme_bw() +
  theme(legend.position = "none")
```

![](draft_files/figure-markdown_github/spaghetti-1.png)

``` r
# ICD-10: bar graph of proportions of each ICD-10 code to determine which ICD-10 diagnosis accounts for the greatest burden of disease in our population. We can potentially facet by sex to see if the burden is different for males and females. 
bar_graph = 
  wave_3_data %>% 
  select(ICD10_01:ICD10_16)
```
