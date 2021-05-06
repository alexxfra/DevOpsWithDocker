# Missing dependencies
The original command:  

`docker run -it --name curler ubuntu sh -c 'echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'`                         
Won't work because curl is not installed. This can be fixed by installing curl beforehand:  

`docker run -it --name curly ubuntu sh -c 'apt update -qq; apt-get install curly -qq > /dev/null; echo "Input website:"; read website; echo "Searching.."; sleep 1; curl http://$website;'`
