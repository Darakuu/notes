Unit tests sono per codice che deve sopravvivere a lungo nel tempo.
E.G. per giochi: saving systems, inventario, etc etc. Sistemi che puoi drag droppare nei progetti

- saving/loading games.
- damage/hitpoints
- apply stats from equipment
- scoring
- changing state
- making sure a locked door doesn't open if you don't have a key
- making sure level-end logic kicks in when you defeat a boss
- ammo

They are also great for fixing bugs. If you can write a failing test the replicates the scenario for the bug, then you don't have to manually test that again. You can also be sure you don't re-introduce it later, once your test starts passing.

Writing tests should help you move faster (though it can seem slower at first) and give you more confidence in your code. I would suggest that you be mindful of how much manual testing you are doing when you implement a feature. Then think about how automating that testing might speed things up. It can be an acquired taste. But once you get into that fail/pass/refactor loop, you really start to appreciate how fast it can be to write tests and, more importantly, how much confidence you have that your code is working. It took me awhile to get to this point, but now I wouldn't know how to live without the safety net and reassurance I get from a good set of tests.

Lastly, the MOST important part of writing a test is that IT MUST FAIL FIRST (there are some exceptions, but 99% should fail first). If you write a passing test, how do you know what you tested?

