# OpenLane CPU Test

A test of building a CPU using OpenLane

## Usage

To build, use `OpenLane` and run the following:

```
PYTHONPATH=$VIRTUAL_ENV/lib/python3.10/site-packages/ \
STD_CELL_LIBRARY_OPT=sky130_fd_sc_hd \
STD_CELL_LIBRARY=sky130_fd_sc_hd \
PDK_ROOT=[path-to-pdk] \
PDK=sky130B \
$OPENLANE_ROOT/flow.tcl \
-design . \
-ignore_mismatches
```

## Notes

This design appears to get stuck in the `abc` step. So far, I have only allowed `yosys-abc` to run for eight hours on a 5900 CPU.
