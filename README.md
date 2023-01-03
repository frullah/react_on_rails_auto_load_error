# Reproducing react_on_rails packs generation error

react_on_rails packs generation command will crash if the public server bundle is not present

```
Errno::ENOENT: No such file or directory @ rb_sysopen - .../public/packs/server-bundle.js
```

so, we should create an empty public server bundle first

```bash
mkdir -p public/packs
touch public/packs/server-bundle.js
```

Then, we can generate react_on_rails packs

```bash
rake react_on_rails:generate_packs
```

and compile javascript assets with shakapacker

```bash
bin/webpacker
```
