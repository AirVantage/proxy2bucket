# proxy2bucket
> Apache reverse proxy to use behind an ELB to serve the content of an S3 bucket on a given domain name.

## Usage

```sh
    # Build
    docker build -t airvantage/proxy2bucket .

    # Run with av-log container
    sudo docker run -d -p 8081:8081 -p 8080:8080 -e DOMAIN_NAME=your.domain.com -e S3_BUCKET_ENDPOINT=http://your.domain.com.s3-website-eu-west-1.amazonaws.com --name="proxy2bucket" --link av-log:av-log airvantage/proxy2bucket
```


