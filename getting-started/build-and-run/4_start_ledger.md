Now that our backend and UI are built we can run the app in two steps.
The first is to start the DAML ledger in another terminal.

```
cd create-daml-app
daml start
```{{execute T2}}

You will know that the command has started successfully when you see the output:

```INFO  com.daml.http.Main$ - Started server: ServerBinding(/0:0:0:0:0:0:0:0:7575)```

The `daml start` command does a few things:

1. Compiles the DAML code to a DAR file as in the previous `daml build` step.
1. Starts an instance of the [Sandbox](https://docs.daml.com/tools/sandbox.html), an in-memory ledger useful for development, loaded with our DAR.
1. Starts a server for the [HTTP JSON API](https://docs.daml.com/json-api/index.html), a simple way for the UI to communicate with our DAML ledger.

We’ll leave this `daml start` running so it can serve requests to our UI.
