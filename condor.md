As configured in INMEGEN, condor accepts only 15000 jobs submitted at once.

To submit 15000 jobs only, you can execute:

```
bin/targets \
| stest -ve \
| head -n 15000 \
| condor-sub condor.header > condor.sub \
&& condor_submit condor.sub
```
