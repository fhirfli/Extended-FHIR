# FHIR-FLI
The aim of this project is to extend the FHIR format to support Lifestyle and Fitness data retrieved from health applications like Google Fit, HealthKit and Fitbit.
This shows an example of how we created our profile for sleep log :

![capture](https://user-images.githubusercontent.com/13016465/29273226-694f285a-80fb-11e7-8bdf-58bf588a60b1.PNG)
The sleep log consists of nested resources. The DiagnosticReport is the Domain Resource that logically groups the other Observation resources in the bundle. The Observations in the bundle referenced by DiagnosticReport are the various levels of sleep (deep, light, rem, wake) and the sleep duration. Each Observation is further divided into components to represent the count and the minutes for each sleep level. The response received from Fitbit after making an API request for sleep log can be found https://dev.fitbit.com/docs/sleep/.
