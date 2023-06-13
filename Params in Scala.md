I've just started working with Scala and Metals in VSCode. I was delighted to notice the Run and Debug hints showing up in the code, apparently without any need to specify debug ports and the like, in `launch.json`.

It occurred to, though that there is no way to specify command-line parameters. If one tried to use the Args feaute of the `launch.json` it doesn't get passed though to Metals.

Can I propose, therefore, a folder beneath where the source files reside, called, maybe, `.params` or `.args`, and in there, with a 1 to 1 relationship with the source files, files such as `app1.json` to correspond to `app1.scala` in the parent directory, with contents of, say...
```json
{
  "params": 
    [
      "alpha",
      "beta',
      "gamma"
     ]
}
```
(Forgive me if my JSON grammer is a little off here ;-))

These parameters would then be passed forward to the app to be processed by a `main` function in the usual Scala manner.

This approach would have the advantage of being much mre light-weight than a UI based solution and still be very usable in terms of workflow.
