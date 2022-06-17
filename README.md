## Online supplement of: 


## "A closest Benders cut selection scheme for accelerating the Benders decomposition algorithm" <br>(published in *INFORMS Journal on Computing* https://doi.org/10.1287/ijoc.2022.1207)


#### by Kiho Seo<sup>1</sup>, Seulgi Joung<sup>2</sup>, Chungmok Lee<sup>3</sup>, and Sungsoo Park<sup>4</sup>

#### <sup>1</sup> Department of Industrial and Systems Engineering, KAIST, Daejeon, Republic of Korea, emffp1410@kaist.ac.kr

#### <sup>2</sup> Department of Industrial Engineering, Chonnam National University, Gwangju, Republic of Korea, sgjoung@jnu.ac.kr

#### <sup>3</sup> Department of Industrial and Management Engineering, Hankuk University of Foreign Studies, Youngin-si, Republic of Korea, chungmok@hufs.ac.kr

#### <sup>4</sup> Department of Industrial and Systems Engineering, KAIST, Daejeon, Republic of Korea, sspark@kaist.ac.kr

------------------------------------------------------------------------

#### This supplement provides instances and results of computational tests in Section 6. 

#### 1. Instances
+ #### /networkdesign
  + Multicommodity Capacitated Fixed-charge Network Design problems that were generated using the Mulgen generator.
  + Instance name: `|N|_|A|_|K|_C_F.lp`
  + All instances are given in `.lp` format.
+ #### /SNDlib
  + Survivable fixed telecommunication Network Design library instances(http://sndlib.zib.de)
  + All instances are given in `.lp` format.
+ #### /SNDlib_sp
  + SNDlib instances(http://sndlib.zib.de) with multiple scenarios generated for comparison between the proposed Benders decomposition algorithm and CPLEX. Random demands in the range [*0.7d<sub>k</sub>, 1.3d<sub>k</sub>*], where *d<sub>k</sub>* is the given demand for commodity *k*. All instances are given in `.mps` format.
  + Instances are contained in a folder in which the number of random scenarios is the name. For example, folder `sndlib_sp/10` contains instances with ten random scenarios.
+ #### /nexp.data.tar
  + Network expansion problem instances (https://atamturk.ieor.berkeley.edu/data/additive.variable.upper.bounds/)
  + All instances are given in `.mps` format.

#### 2. Results

+ #### All results are given in `.json` format.
+ #### Instance name: `instancename_method_benderstype_cuttype.json`
  + method: benders, mip
  + benderstype: bnc, tb
  + cuttype: classical, magnanti, yang, fischetti, closest

```jsonc
{
	"probname": instance name,
	"results": [
		{
			"subtime": time spent in solving the Benders subproblems,
			"totaltime": total computational time,
			"nnodes": number of nodes,
			"x0time": time spent in obtaining the feasible point x0,
			"iteration": number of iterations,
			"objval": objective value,
			"feascutnum": number of feasibility cuts,
			"optcutnum": number of optimality cuts
		}
	],
	"algorithm": [
		{
			"cuttype": cut type,
			"benderstype": benders type
		}
	]
}
```

