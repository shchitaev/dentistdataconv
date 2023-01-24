dentistdataconv (Python3)
===============
This is a fork of the original https://github.com/mhe/dentistdataconv
Change: Python3, fix code, add dicom writing, new packages, add requirements.txt


dentistdataconv.py is a simple Python script that converts volumetric dentist
data to better documented volume formats: [nrrd][1], [MetaImage (mhd)][2], and
[nifti (nii)][3], dicom (dcm).

[1]: https://teem.sourceforge.net/nrrd/
[2]: https://www.itk.org/Wiki/MetaIO
[3]: https://nifti.nimh.nih.gov/nifti-1/

Installation with requirements.txt 
------------

	pip3 install -r requirements.txt 

Usage
-----

The -h options shows how to use it:

    Usage: dentistdataconv.py [options] inputdirectory outputbasename
    
    Options:
      -h, --help       show this help message and exit
      -n, --nhdr       write nrrd header (nhdr)
      -m, --metaimage  write metaimage header (mhd)
      -i, --nifti      write nifti file (nii)
      -r, --raw        write raw data to file (used by header files)
	  -d, --dicom      write dicom data to file (used by header files)

For example, the following command, 

    ./dentistdataconv.py -n -m -r /path/to/datadirectory myvolume

License
-------

See LICENSE.
