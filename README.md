# bsub-repeat

To split up a long job into a recurring small job. Use `--` to separate command from bsub args. Example:

```bsub-repeat -o log-%J.out -- foo.sh args```

This job will relaunch every time it stops due to timeout, until it completes successfully or throws an error.

*UPDATE*: Now allows bsub options to be included the header of foo.sh with `#BSUB ...`
