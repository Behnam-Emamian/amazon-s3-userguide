# Amazon S3 multipart upload limits<a name="qfacts"></a>

The following table provides multipart upload core specifications\. For more information, see [Uploading and copying objects using multipart upload](mpuoverview.md)\.


| Item | Specification | 
| --- | --- | 
| Maximum object size | 5 TB  | 
| Maximum number of parts per upload | 10,000 | 
| Part numbers | 1 to 10,000 \(inclusive\) | 
| Part size | 5 MB to 5 GB\. There is no minimum size limit on the last part of your multipart upload\. | 
| Maximum number of parts returned for a list parts request | 1000  | 
| Maximum number of multipart uploads returned in a list multipart uploads request | 1000  | 