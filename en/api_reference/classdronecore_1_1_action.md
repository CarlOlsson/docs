# dronecore::Action Class Reference
`#include: action.h`

----


The [Action](classdronecore_1_1_action.md) class enables simple actions for a drone such as arming, taking off, and landing. 


## Public Types


Type | Description
--- | ---
enum [Result](#classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011) | Possible results returned for commanded actions.
std::function< void([Result](classdronecore_1_1_action.md#classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011))> [result_callback_t](#classdronecore_1_1_action_1af611bba8734802ab2e32711aa5f3d74c) | Callback type for async [Action](classdronecore_1_1_action.md) calls.

## Public Member Functions


Type | Name | Description
---: | --- | ---
| [Action](#classdronecore_1_1_action_1a4d54f66fbb7629198d5d2f5f261261c0) (ActionImpl *impl) | Constructor (internal use only).
| [~Action](#classdronecore_1_1_action_1a6bb0301fecf66d75ca3b27bda25af7f2) () | Destructor (internal use only).
| [Action](#classdronecore_1_1_action_1ae48b0e06ca2b4b7544a10c7734a03f63) (const Action &)=delete | Copy constructor (object is not copyable).
[Result](classdronecore_1_1_action.md#classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011) | [arm](#classdronecore_1_1_action_1a8b8631ea15655f0c922a9ba7d2e1c72c) () const | Arm the drone (synchronous).
[Result](classdronecore_1_1_action.md#classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011) | [disarm](#classdronecore_1_1_action_1ad4b0231afcfebc261a720194f893dcd8) () const | Disarm the drone (synchronous).
[Result](classdronecore_1_1_action.md#classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011) | [kill](#classdronecore_1_1_action_1adc272f46adf4c52fbe7bd091a436b28b) () const | Kill the drone (synchronous).
[Result](classdronecore_1_1_action.md#classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011) | [takeoff](#classdronecore_1_1_action_1ae159c78b1a4056137187dc6e6d878539) () const | Take off and hover (synchronous).
[Result](classdronecore_1_1_action.md#classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011) | [land](#classdronecore_1_1_action_1ad1a50dd7bff99d3099916576efbf8cf6) () const | Land at the current position (synchronous).
[Result](classdronecore_1_1_action.md#classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011) | [return_to_launch](#classdronecore_1_1_action_1a9af73101ce850e37cf7259dcdeda2eb9) () const | Return to the launch (takeoff) position and land (asynchronous).
void | [arm_async](#classdronecore_1_1_action_1a1a27165400d2a8419c2d96a1c0f2aa78) (result_callback_t callback) | Arm the drone (asynchronous).
void | [disarm_async](#classdronecore_1_1_action_1acc0a17411a25f5641ae21046b459e79e) (result_callback_t callback) | Disarm the drone (asynchronous).
void | [kill_async](#classdronecore_1_1_action_1a1d7d09191d9319c7912962b2dd02caa7) (result_callback_t callback) | Kill the drone (asynchronous).
void | [takeoff_async](#classdronecore_1_1_action_1a2aec10a2b14f5e82f05edc6e2feac83e) (result_callback_t callback) | Take off and hover (asynchronous).
void | [land_async](#classdronecore_1_1_action_1a7f10240cde2ff237795e3688802d857b) (result_callback_t callback) | Land at the current position (asynchronous).
void | [return_to_launch_async](#classdronecore_1_1_action_1aa1253c356c7628d329dfa98d78eb39ee) (result_callback_t callback) | Return to the launch (takeoff) position and land (asynchronous).
void | [set_takeoff_altitude](#classdronecore_1_1_action_1adc6f7f6668d3681afa4d820095154c9d) (float relative_altitude_m) | Set takeoff altitude above ground.
float | [get_takeoff_altitude_m](#classdronecore_1_1_action_1a1888deebcc48d906c3c19473596e6fec) () const | Get the takeoff altitude.
void | [set_max_speed](#classdronecore_1_1_action_1abc27410a9b2a938b21ab59c5ef9ee941) (float speed_m_s) | Set vehicle maximum speed.
float | [get_max_speed_m_s](#classdronecore_1_1_action_1ad6c8a98e0c331666c14cb996fa5dc605) () const | Get the vehicle maximum speed.
const [Action](classdronecore_1_1_action.md) & | [operator=](#classdronecore_1_1_action_1a89f6cdf19fc05054fa746ebd3d88e17a) (const Action &)=delete | Equality operator (object is not copyable).

## Static Public Member Functions


Type | Name | Description
---: | --- | ---
const char * | [result_str](#classdronecore_1_1_action_1a1e44fcd1ee2a566a6590ba2a1ab2e6a7) (Result) | Returns a human-readable English string for an [Action::Result](classdronecore_1_1_action.md#classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011).


## Constructor & Destructor Documentation


### Action() {#classdronecore_1_1_action_1a4d54f66fbb7629198d5d2f5f261261c0}
```cpp
dronecore::Action::Action(ActionImpl *impl)
```


Constructor (internal use only).


**Parameters**

* ActionImpl * **impl** - Private internal implementation.

### ~Action() {#classdronecore_1_1_action_1a6bb0301fecf66d75ca3b27bda25af7f2}
```cpp
dronecore::Action::~Action()
```


Destructor (internal use only).


### Action() {#classdronecore_1_1_action_1ae48b0e06ca2b4b7544a10c7734a03f63}
```cpp
dronecore::Action::Action(const Action &)=delete
```


Copy constructor (object is not copyable).


**Parameters**

* const [Action](classdronecore_1_1_action.md) & **** - 

## Member Typdef Documentation


### typedef result_callback_t {#classdronecore_1_1_action_1af611bba8734802ab2e32711aa5f3d74c}

```cpp
typedef std::function<void(Result)> dronecore::Action::result_callback_t
```


Callback type for async [Action](classdronecore_1_1_action.md) calls.


## Member Enumeration Documentation


### enum Result {#classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011}


Possible results returned for commanded actions.


 Value | Description
--- | ---
<span id="classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011ad0749aaba8b833466dfcbb0428e4f89c"></span> `SUCCESS` | Action succeeded. 
<span id="classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011a23514014e50da2b2583cae24ab1ecd88"></span> `NO_DEVICE` | No device is connected. 
<span id="classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011ac77f1f09dab2c0c9980fca7cfae02518"></span> `CONNECTION_ERROR` | Connection error. 
<span id="classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011a802706a9238e2928077f97736854bad4"></span> `BUSY` | Vehicle busy error. 
<span id="classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011a6fa4dbf368cea972db8d9156799d5dbe"></span> `COMMAND_DENIED` | Command refused. 
<span id="classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011a939d986bd1af6a2e1db07a61a60f7ae2"></span> `COMMAND_DENIED_LANDED_STATE_UNKNOWN` | Command refused because landed state is unknown. 
<span id="classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011ad7e95e2842caf0baff502fbd1290fd69"></span> `COMMAND_DENIED_NOT_LANDED` | Command refused because vehicle not landed. 
<span id="classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011a070a0fb40f6c308ab544b227660aadff"></span> `TIMEOUT` | Timeout waiting for Action to complete. 
<span id="classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011a696b031073e74bf2cb98e5ef201d4aa3"></span> `UNKNOWN` | Unspecified error. 

## Member Function Documentation


### arm() {#classdronecore_1_1_action_1a8b8631ea15655f0c922a9ba7d2e1c72c}
```cpp
Result dronecore::Action::arm() const
```


Arm the drone (synchronous).

**Note** Arming a drone normally causes motors to spin at idle. Before arming take all safety precautions and stand clear of the drone!

**Returns**

&emsp;[Result](classdronecore_1_1_action.md#classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011) - Result of request.

### disarm() {#classdronecore_1_1_action_1ad4b0231afcfebc261a720194f893dcd8}
```cpp
Result dronecore::Action::disarm() const
```


Disarm the drone (synchronous).

This will disarm a drone that considers itself landed. If flying, the drone should reject the disarm command. Disarming means that all motors will stop.

**Returns**

&emsp;[Result](classdronecore_1_1_action.md#classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011) - Result of request.

### kill() {#classdronecore_1_1_action_1adc272f46adf4c52fbe7bd091a436b28b}
```cpp
Result dronecore::Action::kill() const
```


Kill the drone (synchronous).

This will disarm a drone irrespective of whether it is landed or flying. Note that the drone will fall out of the sky if you use this command while flying.

**Returns**

&emsp;[Result](classdronecore_1_1_action.md#classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011) - Result of request.

### takeoff() {#classdronecore_1_1_action_1ae159c78b1a4056137187dc6e6d878539}
```cpp
Result dronecore::Action::takeoff() const
```


Take off and hover (synchronous).

This switches the drone into position control mode and commands it to take off and hover at the takeoff altitude set using [set_takeoff_altitude()](classdronecore_1_1_action.md#classdronecore_1_1_action_1adc6f7f6668d3681afa4d820095154c9d).


Note that the vehicle must be armed before it can take off.

**Returns**

&emsp;[Result](classdronecore_1_1_action.md#classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011) - Result of request.

### land() {#classdronecore_1_1_action_1ad1a50dd7bff99d3099916576efbf8cf6}
```cpp
Result dronecore::Action::land() const
```


Land at the current position (synchronous).


**Returns**

&emsp;[Result](classdronecore_1_1_action.md#classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011) - Result of request.

### return_to_launch() {#classdronecore_1_1_action_1a9af73101ce850e37cf7259dcdeda2eb9}
```cpp
Result dronecore::Action::return_to_launch() const
```


Return to the launch (takeoff) position and land (asynchronous).

This switches the drone into RTL mode which generally means it will rise up to a certain altitude to clear any obstacles before heading back to the launch (takeoff) position and land there.

**Returns**

&emsp;[Result](classdronecore_1_1_action.md#classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011) - Result of request.

### arm_async() {#classdronecore_1_1_action_1a1a27165400d2a8419c2d96a1c0f2aa78}
```cpp
void dronecore::Action::arm_async(result_callback_t callback)
```


Arm the drone (asynchronous).

Note that arming a drone normally means that the motors will spin at idle. Therefore, before arming take all safety precautions and stand clear of the drone.

**Parameters**

* [result_callback_t](classdronecore_1_1_action.md#classdronecore_1_1_action_1af611bba8734802ab2e32711aa5f3d74c) **callback** - Function to call with result of request.

### disarm_async() {#classdronecore_1_1_action_1acc0a17411a25f5641ae21046b459e79e}
```cpp
void dronecore::Action::disarm_async(result_callback_t callback)
```


Disarm the drone (asynchronous).

This will disarm a drone that considers itself landed. If flying, the drone should reject the disarm command. Disarming means that all motors will stop.

**Parameters**

* [result_callback_t](classdronecore_1_1_action.md#classdronecore_1_1_action_1af611bba8734802ab2e32711aa5f3d74c) **callback** - Function to call with result of request.

### kill_async() {#classdronecore_1_1_action_1a1d7d09191d9319c7912962b2dd02caa7}
```cpp
void dronecore::Action::kill_async(result_callback_t callback)
```


Kill the drone (asynchronous).

This will disarm a drone irrespective of whether it is landed or flying. Note that the drone will fall out of the sky if you use this command while flying.

**Parameters**

* [result_callback_t](classdronecore_1_1_action.md#classdronecore_1_1_action_1af611bba8734802ab2e32711aa5f3d74c) **callback** - Function to call with result of request.

### takeoff_async() {#classdronecore_1_1_action_1a2aec10a2b14f5e82f05edc6e2feac83e}
```cpp
void dronecore::Action::takeoff_async(result_callback_t callback)
```


Take off and hover (asynchronous).

This switches the drone into position control mode and commands it to take off and hover at the takeoff altitude set using [set_takeoff_altitude()](classdronecore_1_1_action.md#classdronecore_1_1_action_1adc6f7f6668d3681afa4d820095154c9d).


Note that the vehicle must be armed before it can take off.

**Parameters**

* [result_callback_t](classdronecore_1_1_action.md#classdronecore_1_1_action_1af611bba8734802ab2e32711aa5f3d74c) **callback** - Function to call with result of request

### land_async() {#classdronecore_1_1_action_1a7f10240cde2ff237795e3688802d857b}
```cpp
void dronecore::Action::land_async(result_callback_t callback)
```


Land at the current position (asynchronous).


**Parameters**

* [result_callback_t](classdronecore_1_1_action.md#classdronecore_1_1_action_1af611bba8734802ab2e32711aa5f3d74c) **callback** - Function to call with result of request.

### return_to_launch_async() {#classdronecore_1_1_action_1aa1253c356c7628d329dfa98d78eb39ee}
```cpp
void dronecore::Action::return_to_launch_async(result_callback_t callback)
```


Return to the launch (takeoff) position and land (asynchronous).

This switches the drone into RTL mode which generally means it will rise up to a certain altitude to clear any obstacles before heading back to the launch (takeoff) position and land there.

**Parameters**

* [result_callback_t](classdronecore_1_1_action.md#classdronecore_1_1_action_1af611bba8734802ab2e32711aa5f3d74c) **callback** - Function to call with result of request.

### set_takeoff_altitude() {#classdronecore_1_1_action_1adc6f7f6668d3681afa4d820095154c9d}
```cpp
void dronecore::Action::set_takeoff_altitude(float relative_altitude_m)
```


Set takeoff altitude above ground.


**Parameters**

* float **relative_altitude_m** - Takeoff altitude relative to takeoff location in meters

### get_takeoff_altitude_m() {#classdronecore_1_1_action_1a1888deebcc48d906c3c19473596e6fec}
```cpp
float dronecore::Action::get_takeoff_altitude_m() const
```


Get the takeoff altitude.


**Returns**

&emsp;float - takeoff Altitude relative to takeoff location in meters.

### set_max_speed() {#classdronecore_1_1_action_1abc27410a9b2a938b21ab59c5ef9ee941}
```cpp
void dronecore::Action::set_max_speed(float speed_m_s)
```


Set vehicle maximum speed.


**Parameters**

* float **speed_m_s** - Maximum speed in metres/second.

### get_max_speed_m_s() {#classdronecore_1_1_action_1ad6c8a98e0c331666c14cb996fa5dc605}
```cpp
float dronecore::Action::get_max_speed_m_s() const
```


Get the vehicle maximum speed.


**Returns**

&emsp;float - Maximum speed in metres/second.

### operator=() {#classdronecore_1_1_action_1a89f6cdf19fc05054fa746ebd3d88e17a}
```cpp
const Action& dronecore::Action::operator=(const Action &)=delete
```


Equality operator (object is not copyable).


**Parameters**

* const [Action](classdronecore_1_1_action.md) & **** - 

**Returns**

&emsp;const [Action](classdronecore_1_1_action.md) & - 

### result_str() {#classdronecore_1_1_action_1a1e44fcd1ee2a566a6590ba2a1ab2e6a7}
```cpp
static static const char* dronecore::Action::result_str(Result)
```


Returns a human-readable English string for an [Action::Result](classdronecore_1_1_action.md#classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011).


**Parameters**

* [Result](classdronecore_1_1_action.md#classdronecore_1_1_action_1ad92c9d2e08f60f54b17ea0d861339011) **** - 

**Returns**

&emsp;const char * - 