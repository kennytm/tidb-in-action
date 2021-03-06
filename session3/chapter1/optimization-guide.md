# SQL 调优

如果想要进行 SQL 调优，第一步就是能够读懂一条 SQL 语句的执行计划，以了解其在 TiDB 中是如何被执行的。在读懂执行计划后，本章将讲解一些 SQL 优化器原理的内容，并且将和大家介绍执行计划是如何生成的。优化器是数据库系统中一个非常复杂的模块，很多数据库都避免不了索引选错、Join 顺序不优等问题，因此优化器的表现对数据库系统而言至关重要。SQL Hint 是一种用于 SQL 调优的技术，它可以指导优化器的行为，让其在复杂的情况下能够生成出符合开发者意图的执行计划，本章第三节将介绍基于 SQL Hint 的 SQL Plan Management 技术。本章的最后一节将为大家介绍一些 TiDB 系统参数，方便大家对特定场景的 SQL 进行调优。这些参数有些用于控制优化器的优化规则，有些用于控制执行引擎并发参数或 Batch 参数，以使得 SQL 执行的更快。

希望通过本章的描述，能够让大家对于如何调优 SQL 执行速度有所帮助。
