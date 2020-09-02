你好！
很冒昧用这样的方式来和你沟通，如有打扰请忽略我的提交哈。我是光年实验室（gnlab.com）的HR，在招Golang开发工程师，我们是一个技术型团队，技术氛围非常好。全职和兼职都可以，不过最好是全职，工作地点杭州。
我们公司是做流量增长的，Golang负责开发SAAS平台的应用，我们做的很多应用是全新的，工作非常有挑战也很有意思，是国内很多大厂的顾问。
如果有兴趣的话加我微信：13515810775  ，也可以访问 https://gnlab.com/，联系客服转发给HR。
# News
We are putting together plans for future changes. We obviously depend on all of you to take part in the planning for the future of goamz and execution of the plans. Other than the regulare 'issues' and 'pull requests' please also have a look at TODO.md.     
It is inevitable that there will be backward incompatible changes. Please subscribe to the google group to get all the news (it will only be used for announcements, all the technical discussions will happen on github).     
Google group: https://groups.google.com/forum/#!forum/goamz-announcements 



# GoAMZ

[![Build Status](https://travis-ci.org/crowdmob/goamz.png?branch=master)](https://travis-ci.org/crowdmob/goamz)

The _goamz_ package enables Go programs to interact with Amazon Web Services.

This is a fork of the version [developed within Canonical](https://wiki.ubuntu.com/goamz) with additional functionality and services from [a number of contributors](https://github.com/crowdmob/goamz/contributors)!

The API of AWS is very comprehensive, though, and goamz doesn't even scratch the surface of it. That said, it's fairly well tested, and is the foundation in which further calls can easily be integrated. We'll continue extending the API as necessary - Pull Requests are _very_ welcome!

The following packages are available at the moment:

```
github.com/crowdmob/goamz/aws
github.com/crowdmob/goamz/cloudwatch
github.com/crowdmob/goamz/dynamodb
github.com/crowdmob/goamz/ec2
github.com/crowdmob/goamz/elb
github.com/crowdmob/goamz/iam
github.com/crowdmob/goamz/kinesis
github.com/crowdmob/goamz/s3
github.com/crowdmob/goamz/sqs

github.com/crowdmob/goamz/exp/mturk
github.com/crowdmob/goamz/exp/sdb
github.com/crowdmob/goamz/exp/sns
```

Packages under `exp/` are still in an experimental or unfinished/unpolished state.

## API documentation

The API documentation is currently available at:

[http://godoc.org/github.com/crowdmob/goamz](http://godoc.org/github.com/crowdmob/goamz)

## How to build and install goamz

Just use `go get` with any of the available packages. For example:

* `$ go get github.com/crowdmob/goamz/ec2`
* `$ go get github.com/crowdmob/goamz/s3`

## Running tests

To run tests, first install gocheck with:

`$ go get launchpad.net/gocheck`

Then run go test as usual:

`$ go test github.com/crowdmob/goamz/...`

_Note:_ running all tests with the command `go test ./...` will currently fail as tests do not tear down their HTTP listeners.

If you want to run integration tests (costs money), set up the EC2 environment variables as usual, and run:

$ gotest -i
