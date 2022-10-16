[BaikalOS based on Android Ice Cold Project](http://github.com/baikalos2)
====================================


Download the Source
===================

Please read the [AOSP building instructions](https://source.android.com/source/index.html) before proceeding.

Initializing Repository
-----------------------

Repo initialization:

    $ repo init -u https://github.com/baikalos2/platform_manifest.git -b t13.0


sync repo :

    $ repo sync

Some info on how to customize your sync:

  -f, --force-broken    continue sync even if a project fails to sync

  --force-sync          overwrite an existing git directory if it needs to
                        point to a different object directory. WARNING: this
                        may cause loss of data

  -l, --local-only      only update working tree, don't fetch

  -n, --network-only    fetch only, don't update working tree

  -c, --current-branch  fetch only current branch from server

  -j JOBS, --jobs=JOBS  projects to fetch simultaneously (default 4)

  --no-clone-bundle     disable use of /clone.bundle on HTTP/HTTPS

  --no-tags             don't fetch tags

Smallest/fastest sync:

    $ repo sync --no-tags --no-clone-bundle

    Note: we already define -c in our default.xml, so no need to add it

***

Building
--------

After the sync is finished, please read the [instructions from the Android site](https://source.android.com/source/building.html) on how to build.

    . build/envsetup.sh
    brunch


You can also build (and see how long it took) for specific devices like this:

    . build/envsetup.sh
    time brunch angler

Remember to `make clobber` every now and then!


Additonal build info
-------------------------------
https://github.com/baikalos2/vendor_baikalos/blob/t13.0/docs/baikalosInfo.md

