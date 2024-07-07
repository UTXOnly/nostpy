### Event Class
The Event class manages cryptographic events, including their signing, verification, creation, and sending. It also includes querying functionality to request information from WebSocket relays.

### Example Usage


#### Kind4MessageCodec Class
The Kind4MessageCodec class is a codec for encrypting and decrypting messages using ECDH (Elliptic Curve Diffie-Hellman) for key exchange and AES (Advanced Encryption Standard) in CBC mode for encryption.

Example Usage
#### Encrypting a Message
```python
hex_private_key = "your_private_key_hex"
hex_public_key = "recipient_public_key_hex"

codec = Kind4MessageCodec(hex_private_key, hex_public_key)
message = "Hello, this is a secret message!"
encrypted_message = codec.encrypt_message(message)
print(f"Encrypted Message: {encrypted_message}")
```
#### Decrypting a Message
```python
encrypted_message_with_iv = "base64_encoded_encrypted_message?iv=base64_encoded_iv"

codec = Kind4MessageCodec(hex_private_key, hex_public_key)
decrypted_message = codec.decrypt_message(encrypted_message_with_iv)
print(f"Decrypted Message: {decrypted_message}")
```


### Contributing
Feel free to fork this repository and submit pull requests. Contributions are welcome!
