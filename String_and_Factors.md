String\_and\_Factors
================
Clement Mugenzi
10/15/2019

## String manipulation

``` r
string_vec1 = c("my", "name", "is", "jeff")

str_detect(string_vec1, "jeff") # shows the pattern so we be able to replace
```

    ## [1] FALSE FALSE FALSE  TRUE

``` r
str_replace(string_vec1, "m", "M") # replacing letters 
```

    ## [1] "My"   "naMe" "is"   "jeff"

``` r
string_vec2 = c(
  "i think we all rule for participating",
  "i think i have been caught",
  "i think this will be quite fun actually",
  "it will be fun, i think")

str_detect(string_vec2, "^i think") # be specific with ^ to express the start.
```

    ## [1]  TRUE  TRUE  TRUE FALSE

``` r
str_detect(string_vec2, "i think$") # be specific with ^ to express the end.
```

    ## [1] FALSE FALSE FALSE  TRUE

``` r
string_vec3 = c(
  "Y'all remember Pres. HW Bush?",
  "I saw a green bush",
  "BBQ and Bushwalking at Molonglo Gorge",
  "BUSH -- LIVE IN CONCERT!!")

str_detect(string_vec3, "[Bb]ush") # only capital B and lowercase b
```

    ## [1]  TRUE  TRUE  TRUE FALSE

``` r
string_vec4 = c(
  '7th inning stretch',
  '1st half soon to begin. Texas won the toss.',
  'she is 5 feet 4 inches tall',
  '3AM - cant sleep :('
  ) # numbers follow by letter

str_detect(string_vec4, "[0-9][a-zA-Z]")
```

    ## [1]  TRUE  TRUE FALSE  TRUE

``` r
string_vec5 = c(
  'Its 7:11 in the evening',
  'want to go to 7-11?',
  'my flight is AA711',
  'NetBios: scanning ip 203.167.114.66'
  ) # 7 followed any character and 11.

str_detect(string_vec5, "7.11")
```

    ## [1]  TRUE  TRUE FALSE  TRUE

``` r
string_vec6 = c(
  'The CI is [2, 5]',
  ':-]',
  ':-[',
  'I found the answer on pages [6-7]'
  )

str_detect(string_vec6, pattern = "\\[")
```

    ## [1]  TRUE FALSE  TRUE  TRUE
