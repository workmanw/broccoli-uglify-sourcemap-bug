# broccoli-uglify-sourcemap-bug

Reproduction for issue: https://github.com/ember-cli/broccoli-uglify-sourcemap/issues/57

## Steps

```bash
yarn install
ember build --environment=production
cd dist
python -m SimpleHTTPServer 8000
```

Open http://0.0.0.0:8000 in a browser, the app will not load. See errors in the console.

## Changing package

If you update the `package.json` to use `ember-cli-uglify@1.2.0` and repeat the above steps, it will work.
