# sycl-mapping-api-scanner
A utility to help scan the sources of CUDA-SYCL migration projects and to provide a summary report listing unsupported APIs based on the support status of SYCL mapping/migration APIs tracked by Intel SYCLomatic open source project. The database of CUDA migration APIs is stored under https://github.com/oneapi-src/SYCLomatic/tree/SYCLomatic/docs/dev_guide/api-mapping-status

# How to run 
>
> python sycl-mapping-APIs-scanner.py

Brief:
  This utility mainly scans the preset filetypes(.cu, .cuh, .c, .h, .cpp, .hpp, .py and etc..) to find unsupported APIs listed by SYCLomatic project. Reference link(2023-10-12):https://oneapi-src.github.io/SYCLomatic/dev_guide/api-mapping-status.html

  Please specify the folder path using the -p parameter.

  -p <projectfolderpath>     specify the CUDA migration projects folder path.
  --printcsv                 print report(experimental)

Example usages:

    1.python sycl_mapping_APIs_scanner.py -p <cudaproject_folderpath>

    2.python sycl_mapping_APIs_scanner.py --printcsv <examplereport.csv>

# api_migration_status_arrays_20230926.py

This file contains the database of CUDA migration APIs status .csv files stored under https://github.com/oneapi-src/SYCLomatic/tree/SYCLomatic/docs/dev_guide/api-mapping-statusgenerate_api_migration_status.py

These CUDA migration APIs status .csv files are generated by parsing <SYCLomatic_path>/clang/lib/DPCT/*.inc files with the script tool of <SYCLomatic_path>/clang/tools/dpct/generate_api_migration_status.py
