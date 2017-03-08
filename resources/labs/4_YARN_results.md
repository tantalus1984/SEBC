### Testing loop started on Tue Mar 7 13:10:29 EST 2017

### fastest teragen (benefits from >1 mappers)
* Running teragen with i=4, j=2 and k=512
* real  1m14.448s
* user  0m5.786s
* sys   0m0.290s

#### fastest terasort (benefits from >1 mappers, >1 reducers)
* Running terasort with i=2, j=2 and k=512
* real    1m51.813s
* user    0m7.316s
* sys     0m0.333s

### slowest teragen (1 or 2 reducers; reducers does not matter)
* Running teragen with i=1, j=2 and k=512
* real    1m28.374s
* user    0m5.950s
* sys     0m0.281s

### slowest terasort (1 mapper, 1 reducer; reducers do matter)
* Running terasort with i=1, j=1 and k=512
* real    2m19.462s
* user    0m7.948s
* sys     0m0.348s


### Interpretation
* teragen is completely disk I/O-bound. teragen is a map-only MR job.  Adding more mappers adds in to parallelism and reduces execution time.
* It was found that teragen does not benefit from > 2 mappers in this cluster. The reason for this might be the disk I/O boundness. There is only three worker nodes with 1xSSD each. It appears that two mappers are already able to completely saturate the SSDs of the worker. 
* terasort - other than teragen - has a reduce phase. Addign more mappers and more reducers adds in to parallelism and reduces execution time.
* It was found that terasort does not benefit from > 2 mappers >2 reducers in this cluster. The reason for this might again be the disk I/O boundness and the 1xSSD per worker node. It is again assumed that two mappers and 2 reducers are able to completeley saturate the SSDs of the worker. One might ask why there is room for additional two reducers when teragen alrady showd that two mappers completely saturate the SSDs. The answer is that the reducers in terasort are launched just after the map phase. Of course, in bigger clusters, some reducers might start while the map phase is still ongoing (if at least one mapper has finished). However, this effect is not visible in this cluster, because the cluster is too small.




