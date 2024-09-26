# Tips for the EndeavourOS apps

This page provides some useful tips for using the EndeavourOS apps.

## eos-rankmirrors

### Prefer some mirrors

This app ranks the EndeavourOS mirrors into file `/etc/pacman.d/endeavouros-mirrorlist`.<br>
In file `/etc/rankmirrors.conf` you can *prefer* mirrors you know are the best for your location. To do that, add value(s) to this variable, for example:
```
ALWAYS_FIRST_EOS_MIRRORS='moson|de.freedif|funami'   # use single quotes!
```
As you can see, the values are (partial but unique) mirror URLs. With this value, `eos-rankmirrors` will add these mirrors as first in the ranked `endeavouros-mirrorlist` file.

### Reduce the time for ranking

Another useful variable may be EOS_AUTORANK_TIMEOUT which you can use to reduce the time to rank EndeavourOS mirrors. The default is 30 seconds (for ranking *each* mirror), but making this value smaller can reduce the total ranking time.<br>For example:
```
EOS_AUTORANK_TIMEOUT=5      # allows max 5 seconds for each mirror
```

## eos-pacdiff

To disable the initial warning window when starting `eos-pacdiff`, modify the value of variable `EOS_PACDIFF_WARNING` to `"no"` in file `/etc/eos-script-lib-yad.conf`.
