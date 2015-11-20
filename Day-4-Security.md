#“Assessing Organizational Security from the Outside” Tom Montroy, BitSight Technologies
———————————————————————————
#####Check out BitSight insight report
###SSL
* many moving parts: certificates, keys, hashes, ciphers, server configuration
* significant vulnerabilities found in the past couple of years: heartbleed (steal from server real time), poodle, freak, logjam (rest where degradation attacks), you crack one key might open a thousand doors

* first you have a key exchange with bits
* hashes no longer secure, used to sign the certificate, part of the validation process, using MD5 and even MD2

###SSL Validation
* leaf certificate for computer
* issue certificate for server
* root certificate held by your browser

* establish connection with server, get certificate chain, test for presence of vulnerabilities
* SSL tasks website allows you to test

###SSL: most common errors
* allows insecure protocol: SSLv3 72 %
* Insecure signature algorithm: SHA1 66%
* Diffie-Hellman prime is very commonly used 66%
* Allows insecure protocol: SSLv2 56%
* 7% are vulnerable to heartbleed

#####John Matherly

###Final thoughts
* learn a lot about security posture from externally collected data
* SSL is still a major vulnerability

###small set of breach data
* machine in company infected and reaching out to command center

———————————————————————————
#“The secretive zero day exploit market” Adriel Desautels, Netragard

———————————————————————————
#“Designing for Encryption Performance Niall O’Connor, GenoSpace

###Encryption
* PGP Encryption
* AES Decryption is the biggest aspect of this lecture

###Advanced Encryption Algorithm
* KeyExpansion — create round keys from cipher key

* first round
* AddRoundKey — Each byte is XOR’d with each byte of round key

* Full Round
* SubBytes — Each byte was substituted
* ShiftRows — Last three rows of block is shifted cyclically
* MixColumns - Block columns as shifted
* AddRoundKey

###Block Cipher Mode
* electronic codebook (ECB) mode encryption
* only good for under 16 byte

#####Provider Library (BouncyCastle)

###Advanced encryption standard new instructions (AES-NI)
* new instruction to capture all steps in stage of algorithm
* 4 steps down into one execution

#####AES-NI impacted on Key Length

#####serialization and sorting is what slows down

###conclusion
* cipher block mode
* key length is not a factor, use strongest possible
* encryption not an application bottleneck
* scalable data encryption

———————————————————————————
#“Unobtrusive Intrusion Detection in the Cloud” Running an IDS in OpenStack
Dan Lambright, Red Hat

###Network IDS (NIDS) on openstack
* Design options
* Network Plumbing
* Performance

###Host IDS (HIDS): capabilities uses cases in opensteck
* network and host IDS at the same time

###analyze packets on arrival in real time “active response”

###signature based NIDS
* rules look for patterns in traffic
* community maintains “rule sets”
* using SNORT

###anomaly based NIDS
* deviations from expected behavior trigger, denial of service attack, script based

* ”shellshocked” rule

###use cases for NIDS in OpenStack
###Tenant administrator (IDSaas)
* NIDS guards instance in tenant, NIDS runs instance; tenant is charged

###Hypervision administrator
* NIDS guards all tenants can touch hardware

#####BR-int

###NIDS on compute node
* run in band to user packet flow
* pro: can set up without charge to underlying infrastructure
* con: obtrusive ! NIDS slows traffic

###Mirror traffic to NIDS
* pro: faster, IDS out of band
* con: node’s core allocated to process traffic, need to allocate extra resources aka a CPU core rather than for your tenants or users

#####Add tap integration bridge

###Performance
* undesirable to drop packets when CPU limit hit
* false negatives
* fan-in from instances to the NIDS

#####Snort network IDS

###Open vSwitch performance
* Fast path in kernel: caches flows (large “CAM” table), latest code (>2,1) “screamingly fast
* slow path in user space (ovs-switchd) for new flows
* copies traffic
