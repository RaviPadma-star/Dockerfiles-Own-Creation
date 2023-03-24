-- its a environment variable like key value pairs..
docker build -t env .
docekr images
docker inspect <image id>
docker run env:Environmenttag env
results: PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
HOSTNAME=065e0c994c55
AUTHOR=PADMARAVI
DURATION=90 HOURS
COURSENAME=KUBERNATES
HOME=/root

    --> To overide any of env variable we can use
    	-- docker run -e DURATION=30HRS env:Environmenttag env
    		res: DURATION=30HRS
