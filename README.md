# dsprofiler
Package to profile the major stages of dataset generation, tracking the time elapsed and dataset size per stage.

## Potential API ##

### Create a profiler: ###
prof <- dsprofiler(name = "imaginary dataset", echo = TRUE)

### profile a dataset: ###
with_profiler(prof({
  imaginary_dataset <-
    step1() %>%
    step2() %>%
    step3() %>%
    step4()
})

### plot the time taken and dataset sizes ###
plot(prof)

### create a tibble of times and sizes per steps ###
as_tibble(prof)

### In addition, built-in logging functionality would be great. ###
