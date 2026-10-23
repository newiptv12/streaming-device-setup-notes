# Error codes when a live TV app won't sign in or play

Most streaming apps sit on top of HTTP, so the codes they show follow the HTTP standards. Codes in the 400 range point at the request (your details, your settings or the network you're on). Codes in the 500 range point at the server.

| Code | Meaning | First thing to check |
|---|---|---|
| 401 Unauthorized | Credentials missing or not accepted | Retype the username and password; no extra spaces or auto-capitals |
| 403 Forbidden | Identified, but access refused | Account status; whether another screen is already streaming (many plans allow one stream at a time) |
| 404 Not Found | Nothing at the requested address | The server or portal address saved in the app |
| 410 Gone | Removed on purpose | Request an updated address from the provider |
| 500 / 502 | Server-side fault | Note the time and retry later |
| 503 Service Unavailable | Temporary overload or maintenance | Wait, then retry once |
| 511 Network Authentication Required | The Wi-Fi network wants you to sign in | Open a browser on the device and accept the network's sign-in page |

## Notes

**401 vs 403.** 401 is an identity problem; 403 is a permission problem with a known identity. Retyping only helps with 401.

**404 vs 410.** A 404 doesn't say whether the missing thing is temporary or permanent. A server that knows it was removed for good should send 410. In apps, a 404 usually means a typo in the server address.

**503 and Retry-After.** A 503 is temporary by definition. The server may send a `Retry-After` header, either as an HTTP date or as a number of seconds. Few apps show it, but the meaning holds: nothing on the device needs fixing.

**511.** Typical of guest Wi-Fi in hotels, cafés and offices that shows a welcome or terms page first. The app's own login is not the problem.

**No code, just a message?** Copy the exact wording. Also check the device's date and time are set automatically, because secure connections fail when the clock is wrong.

## What to include in a support request

Code or exact message · time · device model · app version · which other apps still work there · fixes already tried.

## Sources

- RFC 9110, HTTP Semantics, §15 (status codes, incl. §15.6.4 for 503): https://www.rfc-editor.org/rfc/rfc9110.txt
- RFC 6585, §6 (511 Network Authentication Required): https://www.rfc-editor.org/rfc/rfc6585.txt
- MDN, 404 Not Found: https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Status/404
- MDN, Retry-After: https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/Retry-After
