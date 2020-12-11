To test:

1. `cd functions && npm run build && cd -`
1. replace `$PROJECT` with your project name in `public/index.html`
1. `firebase emulators:start --only hosting,auth,functions`
1. open `localhost:5000`, enter phone number
1. come back to logs, get auth code, enter auth code

At this point:

1. observe auth library calling to `authcallback` function (at `localhost:5001`)
1. `authcallback` responds with 302
1. browser ends up on `localhost:5000/done.html`
