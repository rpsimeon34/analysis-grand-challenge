# Datasets from 2015 CMS Open Data release

Given a record id (e.g. `19980`), the list of all datasets can be found with the [`cernopendata-client`](https://cernopendata-client.readthedocs.io/):
```bash
cernopendata-client get-file-locations --protocol xrootd --recid 19980
```
Metadata can be extracted via `get-metadata`.

`datasets.txt` contains a list of folders to help identify relevant physics processes (`list-directory` with `cernopendata-client`).
Relevant records can be found on the [Open Data portal](https://opendata.cern.ch/).

`create_file_list.sh` is a helper script to more conveniently create file lists for a list of records.

## Samples categorized by process

- **ttbar**:
  - nominal:
    - [19980](https://opendata.cern.ch/record/19980): Powheg + Pythia 8 (ext3), 2413 files, 3.4 TB -> converted
    - [19981](https://opendata.cern.ch/record/19981): Powheg + Pythia 8 (ext4), 4653 files, 6.4 TB -> converted
  - scale variation:
    - [19982](https://opendata.cern.ch/record/19982): same as below, unclear if overlap
    - [19983](https://opendata.cern.ch/record/19983): Powheg + Pythia 8 "scaledown" (ext3), 902 files, 1.4 TB -> submitted
    - [19984](https://opendata.cern.ch/record/19984): same as below, unclear if overlap
    - [19985](https://opendata.cern.ch/record/19985): Powheg + Pythia 8 "scaleup" (ext3), 917 files, 1.3 TB -> submitted
  - ME variation:
    - [19977](https://opendata.cern.ch/record/19977): same as below, unclear if overlap
    - [19978](https://opendata.cern.ch/record/19978): aMC@NLO + Pythia 8 (ext1), 438 files, 647 GB -> submitted
  - PS variation:
    - [19999](https://opendata.cern.ch/record/19999): Powheg + Herwig++, 443 files, 810 GB -> submitted

- **single top**:
  - s-channel:
    - [19394](https://opendata.cern.ch/record/19394): aMC@NLO + Pythia 8, 114 files, 76 GB
  - t-channel:
    - [19406](https://opendata.cern.ch/record/19406): Powheg + Pythia 8 (antitop), 935 files, 1.1 TB
    - [19408](https://opendata.cern.ch/record/19408): Powheg + Pythia 8 (top), 1571 files, 1.8 TB
  - tW:
    - nominal:
      - [19412](https://opendata.cern.ch/record/19412): Powheg + Pythia 8 (antitop), 27 files, 30 GB
      - [19419](https://opendata.cern.ch/record/19419): Powheg + Pythia 8 (top), 23 files, 30 GB
    - DS:
      - [19410](https://opendata.cern.ch/record/19410): Powheg + Pythia 8 DS (antitop), 13 files, 15 GB
      - [19417](https://opendata.cern.ch/record/19417): Powheg + Pythia 8 DS (top), 13 files, 14 GB
    - scale variations:
      - [19415](https://opendata.cern.ch/record/19415): Powheg + Pythia 8 "scaledown" (antitop), 11 files, 15 GB
      - [19422](https://opendata.cern.ch/record/19422): Powheg + Pythia 8 "scaledown" (top), 13 files, 15 GB
      - [19416](https://opendata.cern.ch/record/19416): Powheg + Pythia 8 "scaleup" (antitop), 12 files, 14 GB
      - [19423](https://opendata.cern.ch/record/19423): Powheg + Pythia 8 "scaleup" (top), 13 files, 14 GB

    - there are also larger `NoFullyHadronicDecays` samples: [19411](https://opendata.cern.ch/record/19411), [19418](https://opendata.cern.ch/record/19418)
  - tZ / tWZ: potentially missing in inputs, not included in `/ST_*`