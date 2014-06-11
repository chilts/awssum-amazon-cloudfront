NOTE: AwsSum is now deprecated. Please use [aws-sdk](https://www.npmjs.org/package/aws-sdk) instead.

# awssum-amazon-cloudfront #

This is an ```AwsSum``` plugin!

You'll need to add [awssum-amazon-cloudfront](https://github.com/awssum/awssum-amazon-cloudfront/) to your package.json
dependencies. Both [awssum](https://github.com/awssum/awssum/) and
[awssum-amazon](https://github.com/awssum/awssum-amazon/) are pulled in as peer dependencies.

## Example ##

To list all your distributions:

```
var fmt = require('fmt');
var amazonCloudFront = require('awssum-amazon-cloudfront');

var cf = new amazonCloudFront.CloudFront({
    'accessKeyId'     : process.env.ACCESS_KEY_ID,
    'secretAccessKey' : process.env.SECRET_ACCESS_KEY,
    'region'          : amazonS3.US_EAST_1
});

cf.ListDistributions(function(err, data) {
    fmt.dump(err, 'err');
    fmt.dump(data, 'data');
});
```

# Author #

Written by [Andrew Chilton](http://chilts.org/) - [Blog](http://chilts.org/blog/) -
[Twitter](https://twitter.com/andychilton).

# License #

* [Copyright 2011-2013 Apps Attic Ltd.  All rights reserved.](http://appsattic.mit-license.org/2011/)
* [Copyright 2013 Andrew Chilton.  All rights reserved.](http://chilts.mit-license.org/2013/)

(Ends)
