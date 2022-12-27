# Reproducing react_on_rails packs generation error

## Create a public server bundle first to make react_on_rails packs generation work

```bash
mkdir -p public/packs
touch public/packs/server-bundle.js
```

or react_on_rails packs generation will crash because it can't find the public server bundle

```
Errno::ENOENT: No such file or directory @ rb_sysopen - .../public/packs/server-bundle.js
```

## Generate react_on_rails packs

```bash
rake react_on_rails:generate_packs
```

## Compile javascript assets with shakapacker

```bash
bin/webpacker
```

