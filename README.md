# My_AWS_FROM_SCRATCH
AWS Curriculam 

![image](https://github.com/dineshkohi/My_AWS_FROM_SCRATCH/assets/45698578/8c8541e9-4cac-40bc-b2dd-1ceb9aff451e)


AWS Organization:
![image](https://github.com/dineshkohi/My_AWS_FROM_SCRATCH/assets/45698578/bd8b387e-46fc-44f0-a71d-de1fe47cf437)

Cloud Deployment Models-
1> Private Cloud Deployment  -- On premises
2> Public Cloud Deployment   -- aws, azure, GCP
3> community cloud deployment -- multiple cloud like aws and azur,and GCP
4> Hybrid Cloud Deployment  -- on premises as well as public cloud

Computing- to perform any data manuplation.

1> Interview Question: are we create the instance without key? if yes how to access via putty.
yes we can create the instance without key and access the instance with AWS console only. we can change the settings create the user and password. once user and password created than we can access the intance through Putty.

when .pem and .ppk keys use?
.pem -- when OS is linux in your laptop
.ppk -- when OS is windows in your laptop

@@@@@@@@@@@@@@@@@@@@@@@@@@@@

Conversion of .pe, to .ppk
1> open PuTTYGen and click the Load button
2> Set the filetype to *.* so the AWS PEM file is visible
3> Select your PEM file and PuTTYGen will import it.
4> Click Save Private Key and PuTTYGen will convert the PEM to a PPK file.

 ![image](https://github.com/dineshkohi/My_AWS_FROM_SCRATCH/assets/45698578/4cd24744-9cc4-4d4d-99ea-00cb56a93584)


Upload the .ppk into putty for connection-
1> open putty.
2> go to SSh--> auth-->credentials

![image](https://github.com/dineshkohi/My_AWS_FROM_SCRATCH/assets/45698578/3d120d68-ff3a-441e-8bb3-213fad5b5937)


@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@

Instance Setting:

![Uploading image.png…]()


@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@


How the dig work-
*****************
root servers details link- https://www.iana.org/domains/root/servers


[ec2-user@ip-172-31-30-254 ~]$ dig bescom.com @198.41.0.4

; <<>> DiG 9.16.48-RH <<>> bescom.com @198.41.0.4
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 50568
;; flags: qr rd; QUERY: 1, ANSWER: 0, AUTHORITY: 13, ADDITIONAL: 27
;; WARNING: recursion requested but not available

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 4096
;; QUESTION SECTION:
;bescom.com.                    IN      A

;; AUTHORITY SECTION:
com.                    172800  IN      NS      l.gtld-servers.net.
com.                    172800  IN      NS      j.gtld-servers.net.
com.                    172800  IN      NS      h.gtld-servers.net.
com.                    172800  IN      NS      d.gtld-servers.net.
com.                    172800  IN      NS      b.gtld-servers.net.
com.                    172800  IN      NS      f.gtld-servers.net.
com.                    172800  IN      NS      k.gtld-servers.net.
com.                    172800  IN      NS      m.gtld-servers.net.
com.                    172800  IN      NS      i.gtld-servers.net.
com.                    172800  IN      NS      g.gtld-servers.net.
com.                    172800  IN      NS      a.gtld-servers.net.
com.                    172800  IN      NS      c.gtld-servers.net.
com.                    172800  IN      NS      e.gtld-servers.net.

;; ADDITIONAL SECTION:
l.gtld-servers.net.     172800  IN      A       192.41.162.30
l.gtld-servers.net.     172800  IN      AAAA    2001:500:d937::30
j.gtld-servers.net.     172800  IN      A       192.48.79.30
j.gtld-servers.net.     172800  IN      AAAA    2001:502:7094::30
h.gtld-servers.net.     172800  IN      A       192.54.112.30
h.gtld-servers.net.     172800  IN      AAAA    2001:502:8cc::30
d.gtld-servers.net.     172800  IN      A       192.31.80.30
d.gtld-servers.net.     172800  IN      AAAA    2001:500:856e::30
b.gtld-servers.net.     172800  IN      A       192.33.14.30
b.gtld-servers.net.     172800  IN      AAAA    2001:503:231d::2:30
f.gtld-servers.net.     172800  IN      A       192.35.51.30
f.gtld-servers.net.     172800  IN      AAAA    2001:503:d414::30
k.gtld-servers.net.     172800  IN      A       192.52.178.30
k.gtld-servers.net.     172800  IN      AAAA    2001:503:d2d::30
m.gtld-servers.net.     172800  IN      A       192.55.83.30
m.gtld-servers.net.     172800  IN      AAAA    2001:501:b1f9::30
i.gtld-servers.net.     172800  IN      A       192.43.172.30
i.gtld-servers.net.     172800  IN      AAAA    2001:503:39c1::30
g.gtld-servers.net.     172800  IN      A       192.42.93.30
g.gtld-servers.net.     172800  IN      AAAA    2001:503:eea3::30
a.gtld-servers.net.     172800  IN      A       192.5.6.30
a.gtld-servers.net.     172800  IN      AAAA    2001:503:a83e::2:30
c.gtld-servers.net.     172800  IN      A       192.26.92.30
c.gtld-servers.net.     172800  IN      AAAA    2001:503:83eb::30
e.gtld-servers.net.     172800  IN      A       192.12.94.30
e.gtld-servers.net.     172800  IN      AAAA    2001:502:1ca1::30

;; Query time: 0 msec
;; SERVER: 198.41.0.4#53(198.41.0.4)
;; WHEN: Mon May 06 11:54:55 UTC 2024
;; MSG SIZE  rcvd: 835

[ec2-user@ip-172-31-30-254 ~]$ dig bescom.com @192.41.162.30

; <<>> DiG 9.16.48-RH <<>> bescom.com @192.41.162.30
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 38174
;; flags: qr rd; QUERY: 1, ANSWER: 0, AUTHORITY: 2, ADDITIONAL: 3
;; WARNING: recursion requested but not available

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 4096
;; QUESTION SECTION:
;bescom.com.                    IN      A

;; AUTHORITY SECTION:
bescom.com.             172800  IN      NS      ns1.bodis.com.
bescom.com.             172800  IN      NS      ns2.bodis.com.

;; ADDITIONAL SECTION:
ns1.bodis.com.          172800  IN      A       185.85.196.36
ns2.bodis.com.          172800  IN      A       199.59.243.150

;; Query time: 19 msec
;; SERVER: 192.41.162.30#53(192.41.162.30)
;; WHEN: Mon May 06 11:55:46 UTC 2024
;; MSG SIZE  rcvd: 113

[ec2-user@ip-172-31-30-254 ~]$ dig bescom.com @185.85.196.36

; <<>> DiG 9.16.48-RH <<>> bescom.com @185.85.196.36
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 12228
;; flags: qr aa rd; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1
;; WARNING: recursion requested but not available

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 1232
;; QUESTION SECTION:
;bescom.com.                    IN      A

;; ANSWER SECTION:
bescom.com.             10800   IN      A       199.59.243.225

;; Query time: 9 msec
;; SERVER: 185.85.196.36#53(185.85.196.36)
;; WHEN: Mon May 06 11:56:12 UTC 2024
;; MSG SIZE  rcvd: 55

[ec2-user@ip-172-31-30-254 ~]$





