# bandwidth2

Monitor bandwidth usage.
This is a C version of the bandwidth blocklet.

![](bandwidth2.png)

It comes with some other features though:
* Automatically estimate what unit (K,M,G,T) to use depending on the value. You can still choose between bits and bytes.
* By default sum all the network interfaces (except lo) instead of only default route interface.
* Warning and critical colors as an option.

## Build

```
make
```

### Config
```ini
[bandwidth]
label=
command=$SCRIPT_DIR/bandwidth2 
interval=persist
markup=pango
#INTERFACE=(checks all interfaces)
#USE_BITS=0
#USE_BYES=1
#WARN_RX=0
#WARN_TX=0
#CRIT_RX=0
#CRIT_TX=0
```

E.g.

```ini
[bandwidth]
label=
command=$SCRIPT_DIR/bandwidth2 
interval=persist
markup=pango
WARN_RX=307200
WARN_TX=30720
CRIT_RX=512000
CRIT_TX=51200
```
