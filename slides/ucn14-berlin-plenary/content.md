<!-- .slide: class="title" -->

<p style="padding: 5ex 0"> </p>

# WP1 Report

Jon Crowcroft <small>University of Cambridge</small>
[@tforcworc](https://twitter.com/tforcworc)

Richard Mortier <small>University of Nottingham<small>for now...</small></small>
[@mort\_\_\_](https://twitter.com/mort___)

<http://decks.openmirage.org/ucn13-berlin-plenary>

<small>
  Press &lt;esc&gt; to view the slide index, and the &lt;arrow&gt; keys to
  navigate.
</small>


----

## Outline

+ WP1 recap and summary

+ Resources summary
<i>
<div style="font-size: smaller">
<table>
<tr>
<td>Thomas Leonard</td><td>12PM WP1</td><td>cubieboard/arm/mirage</td><td>D1.1 PIH Architecture M9</td>
</tr><tr>
<td>Carlos Molina-Jimenez</td><td>11PM WP4</td><td></td><td>D4.1 Security/Ethics M12</td>
</tr><tr>
<td>JonC+Carlos</td><td>1PM + 1PM WP5</td><td></td><td>D5.1 Use Cases M9</td>
</tr></table>
</div>
</i>

+ Irmin status update


----

<p class="stretch center">
  <object data="ucn-wp1.txt"
    type="text/plain"
    width="980px" height="620px">
  </object>
</p>


<p class="stretch center">
  <object data="ucn-wp1.1.pdf#zoom=50%"
    type="application/pdf"
    width="980px" height="620px">
  </object>
</p>


----

## Irmin

**What's new?**

- July: blog post [[0][]]
- July/August, 2 interns working on the project (synchronisation and merging)
- Sept: Presentation to the OCaml workshop [[1][][1'][]] and submission to
  JFLA [[2][]]
- 2 main users: Citrix (Irmin + Xenstore) [[3][]] and Gregory's imap server
  [[4][]]

[0]: http://openmirage.org/blog/introducing-irmin
[1]: https://ocaml.org/meetings/ocaml/2014/ocaml2014_11.pdf
[1']: https://ocaml.org/meetings/ocaml/2014/irmin-slides.pdf
[2]: http://gazagnaire.org/pub/JFLA14-draft.pdf
[3]: http://openmirage.org/blog/introducing-irmin-in-xenstore
[4]: https://github.com/gregtatcam/imaplet-lwt


## Irmin

**Improved Sync**

- Matthieu Journault (ENS Cachan): Synchronisation of Irmin hosts
- use bloom filters to improve synchronisation performance between Irmin
  instances
- report is available at [[5][]] and slides at [[6][]]
- incremental algorithm, optimised for synchronising graphs with small diffs
- implementation not available in Irmin yet

[5]: http://gazagnaire.org/pub/2014.08.irmin-sync.pdf
[6]: http://gazagnaire.org/pub/2014.08.irmin-sync-slides.pdf


## Irmin

**Improved Merges**

- Benjamin Farinier (ENS Lyon): Mergeable data-structures
- design purely functional data-structures with merge operations
- slides are available at [[7][]] (the report turned into [[2][]])
- code available freely:
  - mergeable queues (opam install merge-queues [[8][]])
  - mergeable ropes (opam install merge-ropes [[9][]])

[2]: http://gazagnaire.org/pub/JFLA14-draft.pdf
[7]: http://gazagnaire.org/pub/2014.08.irmin-merge-slides.pdf
[8]: https://github.com/mirage/merge-queues
[9]: https://github.com/mirage/merge-ropes


## Irmin

**What's Next?**

1. Irmin unikernels (90% completion)
2. Irmin high-level JSON API. (50% completion, the low-level API is there since
   0.3.0)
3. Write a mirage Git server (50% completion, need to fill the server protocol
   logics).

_1+3 == `git pull <unikernel>` to get the state of a running unikernel
(can already do this with a custom, inefficient sync protocol)._


## Irmin

**What's Next?**

1. Irmin unikernels (90% completion)
2. Irmin high-level JSON API. (50% completion, the low-level API is there since
   0.3.0)
3. Write a mirage Git server (50% completion, need to fill the server protocol
   logics).
4. Write a distributed log server or other simple app (not started)
5. Workaround / design a proper solution for bounded storage needs (not started)


----

<p style="font-size: 48px; font-weight: bold;
          display: float; padding: 10ex 0; text-align: center">
  Thanks for listening! Questions?
  <br />
  Contributions very welcome at [openmirage.org](http://openmirage.org)
</p>
