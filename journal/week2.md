# Week 2 — Distributed Tracing

## WEEK SUMMARY
1. I was able to follow up in class and implemented Traces using HoneyComb and Xray
2. I had issues with exporting environmental variables.

Both 

```
export env
```
and
```
gp env 
```

didnt work. So i had to set My ROLLBAR environ variable directly in the docker-compose.yml file

## HOMEWORK CHALLENGE

For the homework challange i was able to add a custom span attribute called "app.http.method" in which i used to get the request time of activities/home route. The code i used is thus:

```
tracer = trace.get_tracer("home.activities")
@app.route("/api/activities/home", methods=['GET'])
def data_home():
  with tracer.start_as_current_span("home-activities-mock-data2"):
    span = trace.get_current_span()
    span.set_attribute("app.http.method", request.method)
    data = HomeActivities.run()
  return data, 200
  ```