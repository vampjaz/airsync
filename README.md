airsync: a simple file synchronization utility using wireless serial bridges
----

You'll need a pair of serial bridge modules, like [these](http://www.hobbyking.com/hobbyking/store/__55560__HKPilot_Transceiver_Telemetry_Radio_Set_V2_915Mhz_.html)

Basically put server.py on the machine with the file you want to sync, then run:

```
python server.py /dev/ttyUSBXX filename.ext
```

with the serial port of the serial bridge and the filename you want to serve.

Then on the client machine, run:

```
python client.py /dev/ttyUSBXX
```

Within a minute or so, the file should be transferred, depending on size. if you leave both programs running, the file will be re-synced if it is changed on the server side.

I am still working on efficiency and have not tested it with binary files yet.
