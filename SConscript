# RT-Thread building script for component

from building import *

cwd = GetCurrentDir()

src = Glob('*.c')

uffs = Split('''
src/uffs/uffs_badblock.c
src/uffs/uffs_blockinfo.c
src/uffs/uffs_buf.c
src/uffs/uffs_debug.c
src/uffs/uffs_device.c
src/uffs/uffs_ecc.c
src/uffs/uffs_crc.c
src/uffs/uffs_fd.c
src/uffs/uffs_find.c
src/uffs/uffs_flash.c
src/uffs/uffs_fs.c
src/uffs/uffs_init.c
src/uffs/uffs_mem.c
src/uffs/uffs_mtb.c
src/uffs/uffs_pool.c
src/uffs/uffs_public.c
src/uffs/uffs_tree.c
src/uffs/uffs_utils.c
src/uffs/uffs_version.c

''')

src = src + uffs
 
CPPPATH = [cwd, cwd + '/src/inc']

group = DefineGroup('Filesystem', src , depend = ['RT_USING_DFS', 'PKG_USING_DFS_UFFS'], CPPPATH = CPPPATH)

Return('group')
