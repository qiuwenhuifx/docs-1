# PG\_AMOP<a name="EN-US_TOPIC_0242385795"></a>

**PG\_AMOP**  records information about operators associated with access method operator families. There is one row for each operator that is a member of an operator family. A family member can be either a search operator or an ordering operator. An operator can appear in more than one family, but cannot appear in more than one search position nor more than one ordering position within a family.

**Table  1**  PG\_AMOP columns

<a name="en-us_topic_0237122268_en-us_topic_0059777617_t24765c48f358468babdb405fd6f019cf"></a>
<table><thead align="left"><tr id="en-us_topic_0237122268_en-us_topic_0059777617_r8c71b5a50d1d46d280b6b4fdc0fa6f82"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="en-us_topic_0237122268_en-us_topic_0059777617_a5c33cbf745c9453cb632f2185431f7f1"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a5c33cbf745c9453cb632f2185431f7f1"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a5c33cbf745c9453cb632f2185431f7f1"></a>Name</p>
</th>
<th class="cellrowborder" valign="top" width="14.66%" id="mcps1.2.5.1.2"><p id="en-us_topic_0237122268_en-us_topic_0059777617_a4079010d515b4e9b860295dedee705d2"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a4079010d515b4e9b860295dedee705d2"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a4079010d515b4e9b860295dedee705d2"></a>Type</p>
</th>
<th class="cellrowborder" valign="top" width="26.69%" id="mcps1.2.5.1.3"><p id="en-us_topic_0237122268_en-us_topic_0059777617_a72e57102813f486aa474e92aa9906f0d"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a72e57102813f486aa474e92aa9906f0d"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a72e57102813f486aa474e92aa9906f0d"></a>Reference</p>
</th>
<th class="cellrowborder" valign="top" width="33.650000000000006%" id="mcps1.2.5.1.4"><p id="en-us_topic_0237122268_en-us_topic_0059777617_ab6e41de6736d463694ecf7adde89bef5"><a name="en-us_topic_0237122268_en-us_topic_0059777617_ab6e41de6736d463694ecf7adde89bef5"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_ab6e41de6736d463694ecf7adde89bef5"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0237122268_en-us_topic_0059777617_rac6433c21d7847eaba9caaaa8ac0b4bb"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_aa0e331f0f9a646438d86f2220a18c777"><a name="en-us_topic_0237122268_en-us_topic_0059777617_aa0e331f0f9a646438d86f2220a18c777"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_aa0e331f0f9a646438d86f2220a18c777"></a>oid</p>
</td>
<td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_ac5bb8f24ba914a4b98adf0ebbb782934"><a name="en-us_topic_0237122268_en-us_topic_0059777617_ac5bb8f24ba914a4b98adf0ebbb782934"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_ac5bb8f24ba914a4b98adf0ebbb782934"></a>oid</p>
</td>
<td class="cellrowborder" valign="top" width="26.69%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a78a98df2ddc64dd8982cc9b10ad05c4d"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a78a98df2ddc64dd8982cc9b10ad05c4d"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a78a98df2ddc64dd8982cc9b10ad05c4d"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="33.650000000000006%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_ad668328afe9e48b5ad88a38a793f82b7"><a name="en-us_topic_0237122268_en-us_topic_0059777617_ad668328afe9e48b5ad88a38a793f82b7"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_ad668328afe9e48b5ad88a38a793f82b7"></a>Row identifier (hidden attribute, which must be specified)</p>
</td>
</tr>
<tr id="en-us_topic_0237122268_en-us_topic_0059777617_r484a132ce8784153a20527e5109a3107"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a2b4579ca37a74000ae44ad7c2dd45586"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a2b4579ca37a74000ae44ad7c2dd45586"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a2b4579ca37a74000ae44ad7c2dd45586"></a>amopfamily</p>
</td>
<td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a459e3ca8495145f6ba18219f01640383"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a459e3ca8495145f6ba18219f01640383"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a459e3ca8495145f6ba18219f01640383"></a>oid</p>
</td>
<td class="cellrowborder" valign="top" width="26.69%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a0036a04f6a10496e966a5cb01c0a9c2a"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a0036a04f6a10496e966a5cb01c0a9c2a"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a0036a04f6a10496e966a5cb01c0a9c2a"></a><a href="pg_opfamily.md">PG_OPFAMILY</a>.oid</p>
</td>
<td class="cellrowborder" valign="top" width="33.650000000000006%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a9357da4617c944028cee2f7ac0a76226"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a9357da4617c944028cee2f7ac0a76226"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a9357da4617c944028cee2f7ac0a76226"></a>Operator family of this entry</p>
</td>
</tr>
<tr id="en-us_topic_0237122268_en-us_topic_0059777617_rc0aae75835f5466eb0796424df8327f2"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a1701ab1f955c4bcbb994ec5a1909bffb"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a1701ab1f955c4bcbb994ec5a1909bffb"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a1701ab1f955c4bcbb994ec5a1909bffb"></a>amoplefttype</p>
</td>
<td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a80d21e7f5c494a008ba901e3b7761f8c"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a80d21e7f5c494a008ba901e3b7761f8c"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a80d21e7f5c494a008ba901e3b7761f8c"></a>oid</p>
</td>
<td class="cellrowborder" valign="top" width="26.69%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_ac6ee0339c861452ebc935bc6f0f65dba"><a name="en-us_topic_0237122268_en-us_topic_0059777617_ac6ee0339c861452ebc935bc6f0f65dba"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_ac6ee0339c861452ebc935bc6f0f65dba"></a><a href="pg_type.md">PG_TYPE</a>.oid</p>
</td>
<td class="cellrowborder" valign="top" width="33.650000000000006%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a1e4d45fb99154eeaba5cb7f09ad3ade8"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a1e4d45fb99154eeaba5cb7f09ad3ade8"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a1e4d45fb99154eeaba5cb7f09ad3ade8"></a>Left-hand input data type of the operator</p>
</td>
</tr>
<tr id="en-us_topic_0237122268_en-us_topic_0059777617_r77f955a33dbd44c181e272790b61786f"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_aa9ce20a269e44885872fe3281a216b45"><a name="en-us_topic_0237122268_en-us_topic_0059777617_aa9ce20a269e44885872fe3281a216b45"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_aa9ce20a269e44885872fe3281a216b45"></a>amoprighttype</p>
</td>
<td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a31fe03226d9c431a920c90d3182d3bb4"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a31fe03226d9c431a920c90d3182d3bb4"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a31fe03226d9c431a920c90d3182d3bb4"></a>oid</p>
</td>
<td class="cellrowborder" valign="top" width="26.69%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_acfd4bb5cf9b348c4bc209cadd78eba6a"><a name="en-us_topic_0237122268_en-us_topic_0059777617_acfd4bb5cf9b348c4bc209cadd78eba6a"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_acfd4bb5cf9b348c4bc209cadd78eba6a"></a><a href="pg_type.md">PG_TYPE</a>.oid</p>
</td>
<td class="cellrowborder" valign="top" width="33.650000000000006%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a41d23917f5344595a96980a46a3068d9"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a41d23917f5344595a96980a46a3068d9"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a41d23917f5344595a96980a46a3068d9"></a>Right-hand input data type of the operator</p>
</td>
</tr>
<tr id="en-us_topic_0237122268_en-us_topic_0059777617_r123c6b79378e4f35bd5b8aa18e564c27"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_aff10bc2961334e5fb5135841a64e5e87"><a name="en-us_topic_0237122268_en-us_topic_0059777617_aff10bc2961334e5fb5135841a64e5e87"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_aff10bc2961334e5fb5135841a64e5e87"></a>amopstrategy</p>
</td>
<td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a31b78a8b9d46410089b3fdd23f7e0e80"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a31b78a8b9d46410089b3fdd23f7e0e80"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a31b78a8b9d46410089b3fdd23f7e0e80"></a>smallint</p>
</td>
<td class="cellrowborder" valign="top" width="26.69%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a3e2980e79f8d4cdaa3e46641f96e971c"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a3e2980e79f8d4cdaa3e46641f96e971c"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a3e2980e79f8d4cdaa3e46641f96e971c"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="33.650000000000006%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a6beace9eb0414701aa8f93611feff0e0"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a6beace9eb0414701aa8f93611feff0e0"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a6beace9eb0414701aa8f93611feff0e0"></a>Number of operator strategies</p>
</td>
</tr>
<tr id="en-us_topic_0237122268_en-us_topic_0059777617_rd6c2503925f24d9c9398eccee694592c"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a0960d6323ae843cbbccc7cd7346a1b2a"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a0960d6323ae843cbbccc7cd7346a1b2a"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a0960d6323ae843cbbccc7cd7346a1b2a"></a>amoppurpose</p>
</td>
<td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a58419e4d45ab48e0bdf9eaa0c0e53539"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a58419e4d45ab48e0bdf9eaa0c0e53539"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a58419e4d45ab48e0bdf9eaa0c0e53539"></a>"char"</p>
</td>
<td class="cellrowborder" valign="top" width="26.69%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a6dacad3a0e944faa82c3cf49ef554cea"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a6dacad3a0e944faa82c3cf49ef554cea"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a6dacad3a0e944faa82c3cf49ef554cea"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="33.650000000000006%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a221000c7989047bf887b7fef1320b6ef"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a221000c7989047bf887b7fef1320b6ef"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a221000c7989047bf887b7fef1320b6ef"></a>Operator purpose, either <strong id="en-us_topic_0237122268_b842352706155531"><a name="en-us_topic_0237122268_b842352706155531"></a><a name="en-us_topic_0237122268_b842352706155531"></a>s</strong> for search or <strong id="en-us_topic_0237122268_b842352706155536"><a name="en-us_topic_0237122268_b842352706155536"></a><a name="en-us_topic_0237122268_b842352706155536"></a>o</strong> for ordering</p>
</td>
</tr>
<tr id="en-us_topic_0237122268_en-us_topic_0059777617_rbd8c364c865c4ba480e72ad727e086e3"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a63285573ea9a47d78146116a20945582"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a63285573ea9a47d78146116a20945582"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a63285573ea9a47d78146116a20945582"></a>amopopr</p>
</td>
<td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a3a04915bcab74aea9ac3d18a0acc5f70"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a3a04915bcab74aea9ac3d18a0acc5f70"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a3a04915bcab74aea9ac3d18a0acc5f70"></a>oid</p>
</td>
<td class="cellrowborder" valign="top" width="26.69%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a18de0ff73e9f4ba682e0143f045b616d"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a18de0ff73e9f4ba682e0143f045b616d"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a18de0ff73e9f4ba682e0143f045b616d"></a><a href="pg_operator.md">PG_OPERATOR</a>.oid</p>
</td>
<td class="cellrowborder" valign="top" width="33.650000000000006%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a0dfb3f34e8e34e6b8e6051945777315a"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a0dfb3f34e8e34e6b8e6051945777315a"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a0dfb3f34e8e34e6b8e6051945777315a"></a>OID of the operator</p>
</td>
</tr>
<tr id="en-us_topic_0237122268_en-us_topic_0059777617_r739c9e1183084e90af43fcf3ac12c8b6"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a9526274cebf047278b2f4e9a0a077c50"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a9526274cebf047278b2f4e9a0a077c50"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a9526274cebf047278b2f4e9a0a077c50"></a>amopmethod</p>
</td>
<td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_aff86c3b41cb644c5ae8bebeae72f628b"><a name="en-us_topic_0237122268_en-us_topic_0059777617_aff86c3b41cb644c5ae8bebeae72f628b"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_aff86c3b41cb644c5ae8bebeae72f628b"></a>oid</p>
</td>
<td class="cellrowborder" valign="top" width="26.69%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a9536814dd0cd48d8b0865d5add961400"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a9536814dd0cd48d8b0865d5add961400"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a9536814dd0cd48d8b0865d5add961400"></a><a href="pg_am.md">PG_AM</a>.oid</p>
</td>
<td class="cellrowborder" valign="top" width="33.650000000000006%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a8bd1803356974da9aeb04b3b79c80651"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a8bd1803356974da9aeb04b3b79c80651"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a8bd1803356974da9aeb04b3b79c80651"></a>Operator family of the index access method</p>
</td>
</tr>
<tr id="en-us_topic_0237122268_en-us_topic_0059777617_r7716b3d50103458ba061d90860870011"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a0a8805d335514857b86c0e69501eb6ac"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a0a8805d335514857b86c0e69501eb6ac"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a0a8805d335514857b86c0e69501eb6ac"></a>amopsortfamily</p>
</td>
<td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_a9b19d44e1e3b48f9955f796c2bad16f1"><a name="en-us_topic_0237122268_en-us_topic_0059777617_a9b19d44e1e3b48f9955f796c2bad16f1"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_a9b19d44e1e3b48f9955f796c2bad16f1"></a>oid</p>
</td>
<td class="cellrowborder" valign="top" width="26.69%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_abcfaedeae31246d39b31cd8032b85a9b"><a name="en-us_topic_0237122268_en-us_topic_0059777617_abcfaedeae31246d39b31cd8032b85a9b"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_abcfaedeae31246d39b31cd8032b85a9b"></a><a href="pg_opfamily.md">PG_OPFAMILY</a>.oid</p>
</td>
<td class="cellrowborder" valign="top" width="33.650000000000006%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0237122268_en-us_topic_0059777617_ae46fd60e4b5d4f1186ea080d773a6e57"><a name="en-us_topic_0237122268_en-us_topic_0059777617_ae46fd60e4b5d4f1186ea080d773a6e57"></a><a name="en-us_topic_0237122268_en-us_topic_0059777617_ae46fd60e4b5d4f1186ea080d773a6e57"></a>The B-tree operator family according to which this entry sorts for an ordering operator (<strong id="en-us_topic_0237122268_b116182410143"><a name="en-us_topic_0237122268_b116182410143"></a><a name="en-us_topic_0237122268_b116182410143"></a>0</strong> for a search operator)</p>
</td>
</tr>
</tbody>
</table>

A search operator entry indicates that an index of this operator family can be searched to find all rows satisfying  **WHERE indexed\_column operator constant**. Obviously, such an operator must return a Boolean value, and its left-hand input type must match the index's column data type.

An ordering operator entry indicates that an index of this operator family can be scanned to return rows in the order represented by  **ORDER BY indexed\_column operator constant**. Such an operator could return any sortable data type, though again its left-hand input type must match the index's column data type. The exact semantics of  **ORDER BY**  are specified by the  **amopsortfamily**  column, which must reference the B-tree operator family for the operator's result type.
