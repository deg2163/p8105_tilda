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
heatmap = wave_3_data %>% 
  select(PH001, PH002) %>% 
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
  
  physical = as.factor(physical), 
  mental = as.factor(mental)
        ) %>% 
  select(-PH001, -PH002)
```
