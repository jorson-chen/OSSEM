# SSH Log

## Description

## Event JSON

```json
{
    "ts": 1463434447.976884,
    "uid": "CWMqft46Ih1Oddh443",
    "id.orig_h": "125.88.177.98",
    "id.orig_p": 51506,
    "id.resp_h": "192.168.1.100",
    "id.resp_p": 22,
    "version": 2,
    "auth_success": false,
    "auth_attempts": 3,
    "client": "SSH-2.0-PUTTY",
    "server": "SSH-2.0-OpenSSH_7.1p2 Debian-1",
    "cipher_alg": "aes128-ctr",
    "mac_alg": "hmac-sha1",
    "compression_alg": "none",
    "kex_alg": "diffie-hellman-group14-sha1",
    "host_key_alg": "ssh-rsa",
    "host_key": "c6:89:9a:8f:05:44:11:0b:cc:1d:5b:1c:31:9b:da:b3",
    "hasshVersion": "1.1",
    "hassh": "92674389fa1e47a27ddd8d9b63ecd42b",
    "hasshServer": "d43d91bc39d5aaed819ad9f6b57b7348",
    "cshka": "ssh-rsa,ssh-dss",
    "hasshAlgorithms": "diffie-hellman-group14-sha1,diffie-hellman-group-exchange-sha1,diffie-hellman-group1-sha1;aes128-ctr,aes192-ctr,aes256-ctr,aes256-cbc,rijndael-cbc@lysator.liu.se,aes192-cbc,aes128-cbc,blowfish-cbc,arcfour128,arcfour,cast128-cbc,3des-cbc;hmac-sha1,hmac-sha1-96,hmac-md5,hmac-md5-96,hmac-ripemd160,hmac-ripemd160@openssh.com;none",
    "sshka": "ssh-rsa,ecdsa-sha2-nistp256,ssh-ed25519",
    "hasshServerAlgorithms": "curve25519-sha256@libssh.org,ecdh-sha2-nistp256,ecdh-sha2-nistp384,ecdh-sha2-nistp521,diffie-hellman-group-exchange-sha256,diffie-hellman-group14-sha1;chacha20-poly1305@openssh.com,aes128-ctr,aes192-ctr,aes256-ctr,aes128-gcm@openssh.com,aes256-gcm@openssh.com;umac-64-etm@openssh.com,umac-128-etm@openssh.com,hmac-sha2-256-etm@openssh.com,hmac-sha2-512-etm@openssh.com,hmac-sha1-etm@openssh.com,umac-64@openssh.com,umac-128@openssh.com,hmac-sha2-256,hmac-sha2-512,hmac-sha1;none,zlib@openssh.com"
}
```

## Data Dictionary

|	        Standard Name       	|            Field Name             |       	    Type            	|   	    Description          	|	     Sample Value           	|
|	-------------------------------	|	-------------------------------	|	-------------------------------	|	-------------------------------	|	-------------------------------	|
|     @timestamp     |     ts               |     date_time     |        Timestamp of the beginning of the event in epoch format     |     `1300475167.096535`  |
|     src_ip_addr     |     id.orig_h     |     ip     |     The originating/source IP address     |     `10.1.1.1`     |
|     src_port     |     id.orig_p          |     integer     |       The originating/source port        |     `37682`     |
|     dst_ip_addr     |     id.resp_h     |     ip     |     The responding/destination IP address     |     `10.2.2.2`     |
|     dst_port     |     id.resp_p          |     integer     |       The responding/destination port        |     `22`     |
|     event_uid     |     uid     |     string     |     Unique ID for the connection.     |     `CHhAvVGS1DHFjwGM9`     |
|     TBD     |     direction     |     string     |     Direction of the connection. If the client was a local host logging into an external host, this would be OUTBOUND. INBOUND would be set for the opposite situation     |     ``     |
|     TBD     |     auth_attempts     |     integer     |     The number of authentication attemps we observed. There’s always at least one, since some servers might support no authentication at all. It’s important to note that not all of these are failures, since some servers require two-factor auth (e.g. password AND pubkey)    |  `` |
|     TBD     |     auth_success     |     boolean     |     Authentication result (T=success, F=failure, unset=unknown)    |   `true`  |
|     TBD     |     cipher_alg     |     string     |     The encryption algorithm in use   |  `aes256-cbc`    |
|     TBD     |     client     |     string     |     The client’s version string   |   `SSH-2.0-1.82 sshlib`   |
|     TBD     |     compression_alg     |     string     |     The compression algorithm in use |    `zlib`  |
|     TBD     |     cshka     |     array_string     |     present if https://github.com/salesforce/hassh is loaded)    |   `ssh-ed25519`   |
|     TBD     |     hassh     |     string     |     present if https://github.com/salesforce/hassh is loaded     |   ``  |
|     TBD     |     hasshAlgorithms     |     array_string     |     present if https://github.com/salesforce/hassh is loaded     |     `curve25519-sha256@libssh.org`   |
|     TBD     |     hasshServer     |     string     |     present if https://github.com/salesforce/hassh is loaded     |   ``  |
|     TBD     |     hasshServerAlgorithms     |     array_string     |     present if https://github.com/salesforce/hassh is loaded     |     `[ "curve25519-sha256@libssh.org", "ecdh-sha2-nistp256" ]`  |
|     TBD     |     hasshVersion     |     string     |     present if https://github.com/salesforce/hassh is loaded     |     `1`  |
|     TBD     |     host_key     |     string     |     The server’s key fingerprint    |   `dd:cc:3a:81:40:2a:fa:9b:eb:7e:24:3d:a2:44:7c:e3`
|     TBD     |     host_key_alg     |     string     |     The server host key’s algorithm |    `ssh-rsa`   |
|     TBD     |     kex_alg     |     string     |     The key exchange algorithm in use    |   `diffie-hellman-group-exchange-sha256`  |
|     TBD     |     mac_alg     |     string     |     The signing (MAC) algorithm in use   |  `hmac-sha2-512` |
|     TBD     |     server     |     string     |     The server’s version string   |   `SSH-2.0-OpenSSH_5.3`   |
|     TBD     |     version     |     integer     |     SSH major version (1 or 2)     |     `2` |
|     TBD     |     remote_location.country_code     |     string     |     The country code     |     ``     |
|     TBD     |     remote_location.region     |     string     |     The region     |     ``     |
|     TBD     |     remote_location.city     |     string     |     The city     |     ``     |
|     TBD     |     remote_location.latitude|double|Latitude     |     ``     |
|     TBD     |     remote_location.longitude|double|Longitude     |     ``     |