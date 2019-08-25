# Configure user accounts

Create users using ansible

## Usage

In group_vars/all, add a list of users with their password and groups:

```yml
users:
  test:
    password: '$6$uGkyWM9PPCCw1OM$JvM3Db3Gjsp20LI7GErCWiJgxiV9coxGSuyuxFMtzF2Qdz/xAJ2G8EV9vsQXs.gVCYrhYxjSh1Vq3v1gievcS1'
    groups:
      - users
      - plugdev
      - sudo
  test2:
    password: '$6$uf5USffF9eaDr0$9PY6Avt4fAw.TzKcqwZBSjopykhrCKPzBArBnnjhZSR6wCu62W7JrLSSNfIWV3lmBC45hLsKFAcDPJEV12Nrv1'
    groups:
      - users
      - plugdev
      - dialout
```

To generate the password strings, use _mkpasswd_ from package _whois_:

  mkpasswd -m sha-512

## License

This project is licensed under the MIT License - see the [LICENSE.md](../LICENSE.md) file for details

