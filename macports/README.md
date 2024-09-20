Open the Portfile, and modify the revision number, for example:

/opt/local/var/macports/sources/rsync.macports.org/macports/release/tarballs/ports/x11/grace

2. sudo port extract grace

3. In the proper folder (see point 1), apply the patches, or modify the
source code. For the patches here attached:

sudo patch -p0 -i patch.diff

4. sudo port configure grace

5. sudo port build grace

6. sudo port destroot grace

7. sudo port install grace

P.S. old_grace-additional_5.1.25.diff: patches obtained from third parties, unvetted and no longer working with C99.


"Extended" patches:
    - Default resolution: 300dpi.
    - Extended vertical toolbar.
    - Coordinate pointer.
    - Wider window at startup (HighRes: 1200; LowRes: 1000).
    - Arrange graphs options are set for larger graph window.
    - View comments set to TRUE.
    - Add buttons quick formula evaluation (single patches attached here, but included in main version grace-ext-full-5.1.25-4.diff)
