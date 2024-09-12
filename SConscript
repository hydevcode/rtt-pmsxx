from building import *
Import('rtconfig')

src   = []
cwd   = GetCurrentDir()

# add pmsxx src files.
src += ['src/pmsxx.c']

if GetDepend('PKG_PMSXX_USING_SENSOR_V1'):
    src += ['src/sensor_plantower_pmsxx.c']

if GetDepend('PKG_USING_PMSXX_SAMPLE'):
    src += Glob('examples/pmsxx_sample.c')

if GetDepend('PKG_USING_SENSOR_V1_PMSXX_SAMPLE'):
    src += Glob('examples/sensor_pmsxx_sample.c')

# add pmsxx include path.
path  = [cwd + '/inc']

# add src and include to group.
group = DefineGroup('pmsxx', src, depend = ['PKG_USING_PMSXX'], CPPPATH = path)

Return('group')
