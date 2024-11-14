Instructions:

1. Install JBang: https://www.jbang.dev/download/
2. Install Camel extension for JBang: https://camel.apache.org/manual/camel-jbang.html#_installation
3. From within this directory, create a Camel template YAML route and run it from your terminal as shown in https://camel.apache.org/manual/camel-jbang.html#_creating_and_running_camel_routes
4. Examine the YAML route and try to conceptualise the flow of events. Read about the:
    * Timer component: https://camel.apache.org/components/4.8.x/timer-component.html
    * Set Body processor: https://camel.apache.org/components/4.8.x/eips/setBody-eip.html
    * Log processor: https://camel.apache.org/components/4.8.x/eips/log-eip.html

Bonus: debug the route as demonstrated in https://camel.apache.org/manual/camel-jbang.html#_camel_route_debugging. Step through each route node and inspect the terminal every time the terminal is suspended.