| Non REST          | REST                                                                                      |
| ----------------- | ----------------------------------------------------------------------------------------- |
| /listAllHubs      | GET /hubs                                                                                 |
| /createHub        | POST /hubs                                                                                |
| /updateHub        | PUT /hubs                                                                                 |
| /deleteHub        | DELETE /hubs/:id                                                                          |
| /listHubMessages  | GET /hubs/:id/messages                                                                    |
| /bubMessageById   | GET /hubs/:id/message/:id                                                                 |
| /countHubMessages | GET /hubs/:id/messages - same endpoint, add an extra property in the response json method |

## req.query

```
https://www.google.com/search?gs_ssp=eJzj4tLP1TdITrY0Ly4xYAQAF0QDXg&q=wreck+it+ralph&oq=wreck+it+r&aqs=chrome.0.46l2j69i57j0l3.4121j0j1&sourceid=chrome&ie=UTF-8
```

```
https://www.google.com/search
?                                     <-- marks the beginning of our query string>
gs_ssp=eJzj4tLP1TdITrY0Ly4xYAQAF0QDXg <-- a key value pair>
&                                     <-- separator for the next key/value pair>
q=wreck+it+ralph                      <-- key value pair>
&                                     <-- so on and so forth>
```

```
req.query = {
  gs_ssp: "eJzj4tLP1TdITrY0Ly4xYAQAF0QDXg"
  q: "wreck+it+ralph"
}
```

`req.query.q` // "wreck+it+ralph"
