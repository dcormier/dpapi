# GO Windows DPAPI Wrapper

The Windows DPAPI uses keys from the user and computer to encrypt data.

Encrypt and decrypt strings:

```
pwd := "password"
encrypted, _ := dpapi.Encrypt(pwd)
decrypted, _ := dpapi.Decrypt(encrypted)
```

Encrypt and decrypt byte arrays:

```
secret := []byte("isolateIndoors")
enc, _ := dpapi.EncryptBytes(secret)
dec, _ := dpapi.DecryptBytes(enc)
```

An encrypted string looks like this: 

AQAAANCMnd8BFdERjHoAwE/Cl+sBAAAAAQ5GMbx570mklMuNAyFRhgAAAAACAAAAAAAQZgAAAAEAACAAAACe7tibTHuzIsKVO2adNjiXU9TM9F1eR95Yk0Wk8Kzj7gAAAAAOgAAAAAIAACAAAAA7quouOuNvn7eicqjE9aa75UZN+TAbokD35hTXbE7UOBAAAADEFNscRxOqxxheOIVdtbiQQAAAAC+UCYzQFtF7uRyhjXKnqCii8OHUtmB5LwIgJTx46uLukKGsOp60rGVPGn6ufiYYCRXiCQPAmQEKjsEE1jwqZto=

References
----------

* [DPAPI on Wikipedia](https://en.wikipedia.org/wiki/Data_Protection_API)
* [Windows Data Protection](https://docs.microsoft.com/en-us/previous-versions/ms995355(v=msdn.10)?redirectedfrom=MSDN) (microsoft.com)
* [Troubleshooting the DPAPI](https://support.microsoft.com/en-us/help/309408/how-to-troubleshoot-the-data-protection-api-dpapi) (microsoft.com)
* [CryptProtectData function](https://docs.microsoft.com/en-us/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) (microsoft.com)
* [Example C Program: Using CryptProtectData](https://docs.microsoft.com/en-us/windows/win32/seccrypto/example-c-program-using-cryptprotectdata) (microsoft.com)

