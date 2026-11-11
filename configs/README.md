# LEDE build configuration

The initial Actions workflow targets the upstream LEDE Airoha AN7581 Nokia XG-040G-MD UBI device profile. Optional modem/QModem and additional packages are being staged separately after confirming they exist in the selected LEDE feeds.

The workflow applies a kernel-version-aware compatibility patch to Quectel's QMI WWAN driver: Linux 6.15 and newer use `hrtimer_setup()`, while older kernels retain `hrtimer_init()`.
