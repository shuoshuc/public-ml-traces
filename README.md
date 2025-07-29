# Public ML traces
The goal of this repo is to organize all the published ML job traces in one place.

Below is a table summarizing what they are, the link to the artifacts and the corresponding paper citation.

|    trace/paper   |                            conference/year                            |                        link to artifacts                        |
|:----------------:|:---------------------------------------------------------------------:|:---------------------------------------------------------------:|
| NCSA Bluewaters |  No publication  |       [link](https://bluewaters.ncsa.illinois.edu/data-sets)       |
| Microsoft Philly |  [ATC'19](https://www.usenix.org/conference/atc19/presentation/jeon)  |       [link](https://github.com/msr-fiddle/philly-traces)       |
|      Helios      |        [SC'21](https://dl.acm.org/doi/10.1145/3458817.3476223)        |     [link](https://github.com/S-Lab-System-Group/HeliosData)    |
|  MIT Supercloud  |        [HPEC'21](https://ieeexplore.ieee.org/abstract/document/9622850)        |     [link](https://dcc.mit.edu/data/)    |
|       Alibaba MLaaS      | [NSDI'22](https://www.usenix.org/conference/nsdi22/presentation/weng) |          [link](https://github.com/alibaba/clusterdata)         |
|        Alibaba FGD       |  [ATC'23](https://www.usenix.org/conference/atc23/presentation/weng)  |          [link](https://github.com/alibaba/clusterdata)         |
|       Acme       |  [NSDI'24](https://www.usenix.org/conference/nsdi24/presentation/hu)  |          [link](https://github.com/InternLM/AcmeTrace)          |
|       Crux       |      [SIGCOMM'24](https://dl.acm.org/doi/10.1145/3651890.3672239)     | [link](https://github.com/alibaba/alibaba-lingjun-dataset-2023) |

Note that the job traces in the NCSA Bluewaters dataset contain GPU allocations. However, it is yet to be confirmed whether the jobs are ML applications or scientific computing.

In case of broken links, a snapshot is taken on July 26, 2025 and hosted on [Zenodo](https://doi.org/10.5281/zenodo.14775936). The archive file is about 4GB.

After downloading the tar.gz file, unzip it with

```bash
tar zxvf trace-snapshot-20250726.tar.gz
```

You will find a folder structure as below:

* **acme/**: Acme trace.
* **alibaba/**: Both Alibaba MLaaS and FGD traces.
* **crux/**: Crux trace.
* **helios/**: Helios trace.
* **philly/**: Microsoft philly trace.
* **supercloud/**: MIT Supercloud trace.
* **bluewaters/**: NCSA Bluewaters trace.

## Trace analysis
A Jupyter notebook is provided for reproducible trace analysis.

In the notebook, there are code snippets that parse, extract, clean up the traces.
You can also find plotting functions in it.
