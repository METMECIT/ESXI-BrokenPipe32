# ESXI-BrokenPipe32
Installation error 32 - Broken Pipe (brand new server) fix

This is an annoying error that is easily resolved.

You only need:

- Name of volume (to increase space)
- ls
- mv
- ln

# How to fix

This fix will place the locker and store as folders in your datastore, effectively giving them TBs of space.

1. at / type:  ls -l
You will see locker and store. Likely locker is linked to store. 

2. type: mv /locker /locker.old

3. type: mv /store /store.old

4. type: ln -s /vmfs/volumes/VolumeName /store

5. type: ln -s /vmfs/volumes/VolumeName /locker

6. type: ls -l (confirm links created)

No more error will occur.
