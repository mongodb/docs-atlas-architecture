|service| auto-scaling adjusts {+cluster+} tier based on real-time resource
usage. The improved auto-scaling engine can now more accurately detect
sustained higher demand and short-term peak traffic for upscaling decisions.
Similarly, |service| makes downscaling choices more promptly, for more
optimized resource utilization and cost profile.

To help control costs, you can specify a range of maximum and minimum
{+cluster+} sizes that your {+cluster+} can automatically scale to.

Auto-scaling works on a rolling basis, meaning the process doesn't
incur any downtime.