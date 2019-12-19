Documentation
=============


[![image](https://img.shields.io/travis/TankerHQ/cloudmesh-transfer.svg?branch=master)](https://travis-ci.org/TankerHQ/cloudmesn-transfer)

[![image](https://img.shields.io/pypi/pyversions/cloudmesh-transfer.svg)](https://pypi.org/project/cloudmesh-transfer)

[![image](https://img.shields.io/pypi/v/cloudmesh-transfer.svg)](https://pypi.org/project/cloudmesh-transfer/)

[![image](https://img.shields.io/github/license/TankerHQ/python-cloudmesh-transfer.svg)](https://github.com/TankerHQ/python-cloudmesh-transfer/blob/master/LICENSE)

see cloudmesh.transfer

* https://github.com/cloudmesh/cloudmesh.transfer

Manual:

* https://github.com/cloudmesh-community/fa19-516-155/blob/master/project/transfer.md

```bash
Usage:
   transfer copy --source=awss3:source_obj --target=azure:target_obj [-r]
   transfer list --target=awss3:target_obj
   transfer delete --target=awss3:target_obj


 This command is part of Cloudmesh's multi-cloud storage service.
 Command allows users to transfer files/directories from storage of
 one Cloud Service Provider (CSP) to storage of other CSP.
 Current implementation is to transfer data between Azure blob
 storage and AWS S3 bucket.
 AWS S3/ Azure Blob storage credentials and container details will
 be fetched from storage section of "~\.cloudmesh\cloudmesh.yaml"


 Arguments:
   awss3:source_obj  Combination of cloud name and the source object name
   source_obj        Source object. Can be file or a directory.
   azure:target_obj  Combination of cloud name and the target object name
   target_obj        Target object. Can be file or a directory.
   transfer_id       A unique id/name assigned by cloudmesh to each
                     transfer instance.


 Options:
   --id=transfer_id            Unique id/name of the transfer instance.
   -h                          Help function.
   --source=aws:source_obj     Specify source cloud and source object.
   --target=azure:target_obj   Specify target cloud and target object.
   -r                          Recursive transfer for folders.


 Description:
   transfer copy --source=<awss3:source_obj>
                 --target=<azure:target_obj> [-r]
       Copy file/folder from source to target. Source/target CSPs
       and name of the source/target objects to be provided.
       Optional argument "-r" indicates recursive copy.

   transfer list --target=awss3:target_obj
       Enlists available files on target CSP at target object

   transfer delete --target=awss3:target_obj
       Deletes target object from the target CSP.

 Examples:
   transfer copy --source=awss3:sampleFileS3.txt
                 --target=azure:sampleFileBlob.txt
```
