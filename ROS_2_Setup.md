# ROS 2 - Network Setup

## Cyclone DDS

Cyclone is not the default DDS implementation, it requires installing. <https://github.com/ros2/rmw_cyclonedds>

Install via package:

```bash
apt install ros-dashing-rmw-cyclonedds-cpp
```

Set as DDS middleware for ROS2:

```bash
export RMW_IMPLEMENTATION=rmw_cyclonedds_cpp
```

Set config parameters (either point to XML file or use XML as a string):

```bash
export CYCLONEDDS_URI=file://$PWD/ros2.xml
```

or

```bash
export CYCLONEDDS_URI='<Discovery><Peers><Peer Address='myroshost.local' /><Peer Address='myroshost2.local' /></></>'
```

Parameters need to be set as multicast does not work when communicating from the N109 LAN to the Wireless Robots.

Sample XML

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<CycloneDDS xmlns="https://cdds.io/config" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation="https://cdds.io/config https://raw.githubusercontent.com/eclipse-cyclonedds/cyclonedds/master/etc/cyclonedds.xsd">
    <Domain id="any">
        <General>
            <NetworkInterfaceAddress>auto</NetworkInterfaceAddress>
            <AllowMulticast>false</AllowMulticast>
            <MaxMessageSize>65500B</MaxMessageSize>
        <FragmentSize>4000B</FragmentSize>
        <Transport>udp4</Transport>
        </General>
    <Discovery>
        <Peers>
            <Peer address="[IPV6-address]"/>
            <Peer address="[IPV6-address]"/>
        </Peers>
        <ParticipantIndex>auto</ParticipantIndex>
    </Discovery>
        <Internal>
            <Watermarks>
                <WhcHigh>500kB</WhcHigh>
            </Watermarks>
        </Internal>
        <Tracing>
            <Verbosity>severe</Verbosity>
            <OutputFile>stdout</OutputFile>
        </Tracing>
    </Domain>
</CycloneDDS>
```

## Firewall Configuration

On the Robots the following command will unblock ROS2 ports for testing:

```bash
sudo firewall-cmd --zone=public --add-port=7400-7450/udp
```

Once this is fully completed need to make these permanent or create a ROS2 services that can be added to the public zone list and do the same for the labs PC'S
