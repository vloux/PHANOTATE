# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.2.2] - 2019-09-08
### Fixed
- An error that was caused by newer versions of tRNAscanSE using the -b flag to indicate a bed file, instead of the earlier versions where this flag was to output brief format.  Using the long arg --brief is compatible with all versions.  
- An error where the ouput from tRNAscanSE with popen was not decoded from bytes to string properly.

## [1.2.1] - 2019-06-06
### Fixed
- An error that was caused by connecting the wrong types of CDS and tRNA in the graph network

### Added
- Displaying the weights (scores) of ORFs in the genbank out file format

## [1.1.1] - 2019-06-06
### Changed
- Excluded tRNA gene calls from tabular and fasta output

### Fixed
- The reporting of tRNAs when the output format is genbank

## [1.1.0] - 2019-06-04
### Added
- Change log

### Changed
- Increased the value of the symbolic INFINITY used in GMP to 1E1000

### Fixed
- Previous versions of the submodule fastpathz had an error in the scientific notation conversion whereby the weight of an edge was put into a character array that was not proprely null \0 terminated. This caused unpredictable behavior sometimes causing the weight to default to zero. 