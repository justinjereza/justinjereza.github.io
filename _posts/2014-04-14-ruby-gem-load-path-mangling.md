---
layout: midnight
---

Ruby gem load path mangling doesn't quite work the way I expect it to. If `foo`
is installed in both `~/.gems/` and `/usr/lib/ruby/`, `require 'foo'` loads the copy
in `/usr/lib/ruby/`. I think the copy in `~/.gems/` should take priority since the
user may choose to override the copy installed in the system itself. If `foo` is
installed only in `~/.gems/`, then the right thing is done and the path to the
gem is added to $LOAD_PATH.
