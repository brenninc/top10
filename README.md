This is a toy example of one way to run several dockerized examples.

It makes uses of two toy docker images

https://github.com/brenninc/top10
https://github.com/brenninc/last5

Then links then together.

1. Create a data folder (here we assume the fullpath to be /tmp/mydata)
2. Add a text file with the numbers 1 to 20 one per line as one_to_twenty.txt
3. docker run -v /tmp/mydata:/data brenninc/top10 /data/one_to_twenty.txt  /data/one_to_ten.txt
4. docker run -v /tmp/mydata:/data brenninc/last5 /data/one_to_ten.txt  /data/six_to_ten.txt
5. ls /tmp/mydata
