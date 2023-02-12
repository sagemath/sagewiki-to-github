# sagewiki

Tools for the Sage wikis.

## convert.py

Master script for converting an existing (SageMath) MoinMoin wiki to a gollum wiki.

## config.ru

Rack script for running gollum with the necessary authentication bits,
and loading the correct modules.

## moin2git and moin2mdwn

These files are modifications of the same-named files from http://ikiwiki.info/tips/convert_moinmoin_to_ikiwiki/

I believe the original authors are Josh Triplett and Antoine Beaupré.

## Licenses

`moin2git` and `moin2mdwn` are probably licensed under the GPLv2 license (see `GPL_LICENSE`).

`unidecode` is vendored in `unidecode`, and is licensed under GPLv2 (see `GPL_LICENSE`).

The rest of everything in this repository is licensed under the MIT license (see `MIT_LICENSE`).

## Converting the Sage wiki to markdown:

This needs python2; pyenv makes it easy to install it.

    pyenv install 2.7
    eval "$(pyenv init -)"
    python -m pip install -r requirements.txt

Symlink the wiki configuration and data (unpacked from an archive):

    ln -s SOMEWHERE/wiki wiki
    ln -s wiki/data data

Start the conversion:

    ./convert.py

This creates a bare repo ``test.git`` and a clone ``test``.
