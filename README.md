# mom6-remapping
f90wrapped MOM6 remapping core

To use the remapping interface from Python:

~~~python
from remapping import mom_remapping
cs = mom_remapping.Remapping_Cs()

# set the interpolation scheme
# 0 = PCM
# 1 = PLM
# 2 = PPM H4
# 3 = PPM IH4
# 4 = PQM IH4 IH3
# 5 = PQM IH6 IH5
cs.interpolation_scheme = <n>

# set the degree depending on the interpolation
# 0 = PCM
# 1 = PLM
# 2 = PPM
# 4 = PQM
cs.degree = <n>

u1 = mom_remapping.remapping_core_h(cs, h0, u0, h1)
~~~
