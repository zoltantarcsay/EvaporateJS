#v1.0.6#

##Fixes##
- Adds the ability to verify the checksum of the first part of an uploaded file. If localStorage file cache indicates that the file has been uploaded, if the Md5 checksums of the the do not match, the file is uploaded rather than reused.

#v1.0.5#

##Features##
- Adds localStorage cache to keep track of files upload state, allowing resumption of incomplete parts
- Adds ability to ignore uploading a file if it can be found in the S3 bucket.

#v1.0.4#

##Fixes##
- Corrects missing error control (and retry) for Initiate and Complete. This satisfies AWS requirement to retry on errors.
- Corrects handling of progress indicator where progress was set to 100% when aborting rather than only when the file is actually complete.

