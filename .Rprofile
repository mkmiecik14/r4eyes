# .RProfile file that prints a message to the console every 20 minutes
# reminding you to take a break for 20 seconds and look at something at least
# 20 feet or farther in the distance

# checks to see if later is installed
if (system.file(package = "later") == "") {
  print("You do not have the package `later` installed")
  print("Please install `later` for this .Rprofile to work.")
  print("install.packages('later')")
}

# rest_eyes function
rest_eyes <- function(m = 20) {
  seconds <- m*60 # later() expects seconds, so this converts arg to seconds 
  print(
    paste(
      "It's been", 
      m, 
      "minutes. Take a 20 second break and look at something at least 20 feet away!"
      )
  )
  later::later(~rest_eyes, seconds) # delays next print to m minutes
}
later::later(~rest_eyes, 20*60) # this delays the first print to 20 min 
