# JMeter sample
A sample of load test with JMeter.

## Script details
### Thread Group
Thread groups manages how many virtual users will request, along with the ramp-up time.

### Http Request
The domain that will be tested is `http://localhost:8080` (can be changed in _Variables for local environment_), and the URI is `/actuator/health` (can be changed in _Actuator Health > HTTP Request_).

### Assertions
There are two assertions that are executed when the test is executed. They verify the response code and the Json content.

If the assertion is failed, an error is displayed in _View Result Tree_.

#### Response code
The _Actuator Health > Response Assertion - Response Code_ verifies if the HTTP Response code is `200`.

#### Json content
The _Actuator Health > JSON Assertion - Status_ verifies if the response file is a Json and if the attribute `status` has value equal to `UP`.
