+++
title = "Dbmigrate, a SQL migration tool"
date = 2016-01-11

[extra]

source = { author = "Keats", link = { url = "https://users.rust-lang.org/t/dbmigrate-a-sql-migration-tool/4242", name = "Rust Users Forum" } }

tags = [
  "database",
  "tooling",
  "dbmigrate"
]

+++

<h2>dbmigrate</h2>

<p><a href="https://github.com/Keats/dbmigrate" class="onebox" target="_blank" rel="nofollow">https://github.com/Keats/dbmigrate</a></p>

<p>I mentioned it before on reddit but since I just released a new version working with MySQL as well, might be worth putting it here.</p>

<p>This is a tool heavily inspired by a Go tool I've used: <a href="https://github.com/mattes/migrate" rel="nofollow">migrate</a> and django migrations.</p>

<p>In short, a migration involves 2 sql files, a <code>up</code> and a <code>down</code> which are plain SQL and are executed depending on what you want do (running <code>dbmigrate up</code> will run all the <code>up</code> migrations not done yet in order for example).</p>

<p>This currently supports PostgreSQL and MySQL, adding a driver is not too hard so let me know if there's another database that could use it.</p>

<p>Also looking for feedback on needed commands I don't have implemented yet and general code review.</p>
