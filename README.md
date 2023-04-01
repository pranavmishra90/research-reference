# Research Reference - An open notebook for lab protocols and materials

The [GitHub repository](https://github.com/pranavmishra90/research-reference) is the primary public-facing repository, while the [GIN repository](https://gin.g-node.org/pranavmishra90/research-reference) hosts annex-files as a common data source. If you would like to view the files without having to clone/download the Datalad dataset, you please visit the [GIN repository](https://gin.g-node.org/pranavmishra90/research-reference).

Current status: Most of my lab protocols documented in my LabArchives Notebooks and also kept on our Microsoft 365 infrastructure. I'm creating this Datalad dataset to try an 'open' format, which doesn't require authentication to view and allows others to comment on the contents.

If you have any questions, comments, or critiques, please do not hesitate to open an [issue on GitHub](https://github.com/pranavmishra90/research-reference/issues). 

<img src="https://img.shields.io/endpoint?url=https%3A%2F%2Fraw.githubusercontent.com%2Fpranavmishra90%2Fbadges%2Fmain%2FRush/BFI/datalad.json&amp;color=3e4c75" alt="datalad">  <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Fraw.githubusercontent.com%2Fpranavmishra90%2Fbadges%2Fmain%2FRush/BFI/python.json&amp;color=3e4c75" alt="python"> <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Fraw.githubusercontent.com%2Fpranavmishra90%2Fbadges%2Fmain%2Fone-sided-badge/jupyter.json&amp;color=3e4c75" alt="jupyter"> <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Fraw.githubusercontent.com%2Fpranavmishra90%2Fbadges%2Fmain%2Fone-sided-badge/anaconda.json&amp;color=3e4c75" alt="anaconda"> <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Fraw.githubusercontent.com%2Fpranavmishra90%2Fbadges%2Fmain%2Fone-sided-badge/labarchives.json&amp;color=3e4c75" alt="labarchives"> <img src="https://img.shields.io/endpoint?url=https%3A%2F%2Fraw.githubusercontent.com%2Fpranavmishra90%2Fbadges%2Fmain%2Ftwo-side-status-badge/pre-commit-enabled.json&amp;color=3e4c75" alt="pre-commit-enabled">

### Repository Maintainer

<strong>Pranav Kumar Mishra, MBBS</strong><br>
Post-Doctoral Research Fellow<br>
Departments of Surgery and Orthopedic Surgery<br>
Rush University Medical Center

Email: pranav\_k\_mishra@rush.edu<br>

<br>

<a href="https://orcid.org/my-orcid?orcid=0000-0001-5219-6269"><img src="https://img.shields.io/endpoint?url=https%3A%2F%2Fraw.githubusercontent.com%2Fpranavmishra90%2Fbadges%2Fmain%2FPranav/orchid.json&amp;color=3e4c75" alt="orchid"></a>
<a href="https://github.com/pranavmishra90"><img src="https://img.shields.io/endpoint?url=https%3A%2F%2Fraw.githubusercontent.com%2Fpranavmishra90%2Fbadges%2Fmain%2FPranav/github.json&amp;color=3e4c75" alt="github"></a>

## About this dataset

### General information

This is a DataLad dataset (id: 3d6beff7-a55d-43a2-ab44-6def6a79bde5).

### DataLad datasets and how to use them

This repository is a [DataLad](https://www.datalad.org/) dataset. It provides
fine-grained data access down to the level of individual files, and allows for
tracking future updates. In order to use this repository for data retrieval,
[DataLad](https://www.datalad.org/) is required. It is a free and open source
command line tool, available for all major operating systems, and builds up on
Git and [git-annex](https://git-annex.branchable.com/) to allow sharing,
synchronizing, and version controlling collections of large files.

More information on how to install DataLad and [how to install](http://handbook.datalad.org/en/latest/intro/installation.html)
it can be found in the [DataLad Handbook](https://handbook.datalad.org/en/latest/index.html).

#### Get the dataset

A DataLad dataset can be `cloned` by running

```
datalad clone <url>
```

Once a dataset is cloned, it is a light-weight directory on your local machine.
At this point, it contains only small metadata and information on the identity
of the files in the dataset, but not actual *content* of the (sometimes large)
data files.

#### Retrieve dataset content

After cloning a dataset, you can retrieve file contents by running

```
datalad get <path/to/directory/or/file>
```

This command will trigger a download of the files, directories, or subdatasets
you have specified.

DataLad datasets can contain other datasets, so called *subdatasets*.  If you
clone the top-level dataset, subdatasets do not yet contain metadata and
information on the identity of files, but appear to be empty directories. In
order to retrieve file availability metadata in subdatasets, run

```
datalad get -n <path/to/subdataset>
```

Afterwards, you can browse the retrieved metadata to find out about subdataset
contents, and retrieve individual files with `datalad get`.  If you use
`datalad get <path/to/subdataset>`, all contents of the subdataset will be
downloaded at once.

#### Stay up-to-date

DataLad datasets can be updated. The command `datalad update` will *fetch*
updates and store them on a different branch (by default
`remotes/origin/master`). Running

```
datalad update --merge
```

will *pull* available updates and integrate them in one go.

#### Find out what has been done

DataLad datasets contain their history in the ``git log``.  By running ``git
log`` (or a tool that displays Git history) in the dataset or on specific
files, you can find out what has been done to the dataset or to individual
files by whom, and when.
