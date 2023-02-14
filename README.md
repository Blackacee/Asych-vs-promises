# Asych-vs-promises

async function doAsyncThing() { ... }
function doPromiseThing(input) { return new Promise((r, x) => ...); }
// Call with promise syntax
doAsyncThing()
 .then(a => doPromiseThing(a))
 .then(b => ...)
 .catch(ex => ...);
// Call with await syntax
try {
 const a = await doAsyncThing();
 const b = await doPromiseThing(a);
 ...
}
catch(ex) { ... }
