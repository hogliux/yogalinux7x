0) export PATH="/usr/lib/rust-1.93/bin:$PATH"
1) fakeroot debian/rules clean
2) debuild -S
3) cd ..
3.5) /etc/pbuilderrc needs to have the following:
EXTRAPACKAGES=fakeroot
USENETWORK=yes
4) pbuilder-dist resolute linux-7.0.0-90.90.dsc
5) result in ~/pbuilder/oracular_result

====
to bnuild locally:
0) export PATH="/usr/lib/rust-1.93/bin:$PATH"
1) fakeroot debian/rules clean
2) fakeroot debian/rules prepare-generi
3) you can then use make in debian/build/build-generic