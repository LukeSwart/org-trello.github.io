---
layout: post
title:  "Migration"
date:   2014-03-16 11:01:52
---

# Migration

## 0.3.1

The old checklist/item format has been removed - https://github.com/org-trello/org-trello/issues/105.
Now the org checkbox way is the standard one.

## 0.2.9

For information, from 0.2.9 onward, the property "orgtrello-id" from the checkbox (checklists, items) will be hidden.

*Note*
- Upon activating org-trello minor mode, all existing checkbox will be migrated and should disappear before your eyes.
- Symmetrically, when deactivating org-trello, all checkbox will appear.
- For this, org-trello use [overlays](https://www.gnu.org/software/emacs/manual/html_node/elisp/Overlays.html) (implementation detail which permits to hide buffer region).

If you began to use org-trello, nothing to do.

## 0.2.8

From 0.2.8 onward, the card description can be synchronized too.
Just synchronize as usual.

## 0.2.1 -> 0.2.2

From the 0.2.2 version onward, we can assign people to card.
As a pre-requisite, we need to re-install the board (C-c o I), so that new properties will be installed (users currently assigned to the board we attach to).

This way, you will be able to use the assign (C-c o a) / unassign (C-c o u) yourself to the card.

## 0.1.5 -> 0.1.6

Org-trello now uses more natural ways of dealing with checklists using checkboxes!

cf. [natural org format (from 0.1.6 onwards)](#natural-org-format-from-016-onwards) for more details.

## 0.1.1 -> 0.1.2

- From version 0.1.1, some http requests will be asynchronous.
For this, we use elnode as a proxy server to make requests to trello.
The elnode server is started on the port 9876.
You can always change this port

``` lisp
(setq *ORGTRELLO-PROXY-PORT* 9876)
```
Then <kbd>M-x orgtrello-proxy/reload</kbd>