Similarly to [NEX](https://github.com/kinnay/NintendoClients/blob/71fe4d65befb5a49874d09a711e1c121a641575e/nintendo/nex/errors.py), UPlay defined its custom result codes in addition to the standard ones, which could be returned as errors to a client.

## Result codes

| Code | Name |
|---|---|
| 0xB0001 | `UPlayResult::INVALID_PARAMETER` |
| 0xB0002 | `UPlayResult::ALREADY_LOGGED_IN` |
| 0xB0003 | `UPlayResult::ALREADY_LOGGING_IN` |
| 0xB0004 | `UPlayResult::CRYPT_FAILURE` |
| 0xB0005 | `UPlayResult::EXPIRED_TICKET` |
| 0xB0006 | `UPlayResult::COULD_NOT_RETRIEVE_NP_TICKET` |
| 0xB0007 | `UPlayResult::USER_LOGGED_OUT` |
| 0xB0008 | `UPlayResult::REQUEST_FAILED` |
| 0xB0009 | `UPlayResult::INVALID_ATTRIBUTE_RESPONSE` |
| 0xB000A | `UPlayResult::INVALID_SESSION_TICKET` |
| 0xB000B | `UPlayResult::INVALID_AUTH_TOKEN` |
| 0xB000C | `UPlayResult::CONTENT_ID_NOT_FOUND` |
| 0xB000D | `UPlayResult::CONTENT_TYPE_NOT_FOUND` |
| 0xB000E | `UPlayResult::MISSING_ATTRIBUTE` |
| 0xB000F | `UPlayResult::TRANSFER_IN_PROGRESS` |
| 0xB0010 | `UPlayResult::REQUEST_FAULTED` |
| 0xB0040 | `UPlayResult::HTTP_INTERNAL_FAILURE` |
| 0xB0041 | `UPlayResult::HTTP_CONNECTION_FAILURE` |
| 0xB0042 | `UPlayResult::HTTP_TRANSACTION_FAILURE` |
| 0xB0043 | `UPlayResult::HTTP_CONNECT_TIMEOUT` |
| 0xB0044 | `UPlayResult::HTTP_SEND_TIMEOUT` |
| 0xB0045 | `UPlayResult::HTTP_RECV_TIMEOUT` |
| 0xB0046 | `UPlayResult::HTTP_ISTREAM_ERROR` |
| 0xB0047 | `UPlayResult::HTTP_OSTREAM_ERROR` |
| 0xB0048 | `UPlayResult::HTTP_SOCKET_ERROR` |
| 0xB0080 | `UPlayResult::SERVICE_INTERNAL_FAILURE` |
| 0xB0081 | `UPlayResult::INVALID_REQUEST` |
| 0xB0082 | `UPlayResult::ACCOUNT_PROBLEM` |
| 0xB0083 | `UPlayResult::CONTENT_DOES_NOT_EXIST` |
| 0xB0084 | `UPlayResult::NO_FREE_SLOT` |
| 0xB0085 | `UPlayResult::NO_PRIVILEGE` |
| 0xB0086 | `UPlayResult::UNSUPPORTED_RATING_TYPE` |
| 0xB0087 | `UPlayResult::OUT_OF_RANGE_RATING` |
| 0xB0088 | `UPlayResult::CONTENT_ALREADY_RATED` |
| 0xB0089 | `UPlayResult::INVALID_TICKET` |
| 0xB008E | `UPlayResult::SSL_ERROR` |
| 0xB008F | `UPlayResult::SSL_ERROR_NO_CERT` |
| 0xB0090 | `UPlayResult::SSL_ERROR_UNKNOWN_CA` |
| 0xB0091 | `UPlayResult::SSL_ERROR_BAD_CHAIN` |
| 0xB0092 | `UPlayResult::SSL_ERROR_INVALID_CERT` |
| 0xB0093 | `UPlayResult::SSL_ERROR_VERIFY_FAILED` |
| 0xB0094 | `UPlayResult::SSL_ERROR_COMMON_NAME` |
| 0xB0095 | `UPlayResult::SSL_ERROR_EXPIRED` |
| 0xB0096 | `UPlayResult::SSL_ERROR_NOT_YET_VALID` |
| 0xB009A | `UPlayResult::INVALID_TOKEN` |
| 0xB009B | `UPlayResult::EXPIRED_TOKEN` |
| 0xB009C | `UPlayResult::KEY_DECRYPTION_FAILED` |
| 0xB009D | `UPlayResult::SERVICE_UNAVAILABLE` |
| 0xB0100 | `UPlayResult::NOT_INITIALIZED` |
| 0xB0101 | `UPlayResult::SYSTEM_OFFLINE` |
| 0xB0102 | `UPlayResult::INVALID_STATE` |
| 0xB0103 | `UPlayResult::NOT_SIGNED_IN` |
