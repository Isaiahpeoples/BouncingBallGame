<h1>Bouncing Ball Game</h1>

<h2>Description</h2>
This project is a game that utilizes the 'tkinter' module within Python to create a bouncing ball and a controllable paddle. To begin playing the game, the player clicks anywhere in the game window. The ball bounces around the screen and the paddle is used to prevent the ball from hitting the bottom of the screen which will cause a GAME OVER. A score counter is located at the top right and it rises each time the ball hits the paddle. To add a bit of difficulty the ball will increase in speed if the paddle is moving in the same direction once it strikes the ball. If the paddle was struck while moving in the opposite direction of the ball, the speed of the ball will decrease.
<br />


<h2>Keywords, Functions, & Utilities Used</h2>

- <b>tkinter module</b> 
- <b>random module</b>
- <b>intialization function</b>
- <b>key bindings</b>
- <b>class</b>
- <b>define</b>
- <b>while</b>
- <b>if</b>
- <b>or</b>

<h2>Project Walk-Through:</h2>


<h3 align="center">Create the canvas:</h3> <br/>
<p align="center">
<img src="https://eastus1-mediap.svc.ms/transform/thumbnail?provider=spo&farmid=194112&inputFormat=png&cs=MDAwMDAwMDAtMDAwMC0wMDAwLTAwMDAtMDAwMDQ4MTcxMGE0fFNQTw&docid=https%3A%2F%2Fmy.microsoftpersonalcontent.com%2F_api%2Fv2.0%2Fdrives%2Fb!6V-MtG_eY0-k9L3oLFYG78uFi7wejWlDtk1uGQBckp1A2A3GGZExRqpoc3ruqnky%2Fitems%2F016IFZ7YOFAZ6QWEKGFRDJFY3QUCJ6FZJL%3Ftempauth%3Dv1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwNTYwMDAifQ.igXvXz1RdGce_zcCPy30i6KVSeMXQ96YRlazY65E8WKlxOQ6FkyEtLIChiG1PWzNd_M-DKaS6FTSZtRLoed2u4OvjEL54p4mlN8yoKrIVSD_TbECvzwzmhSER1TFwp7rg2C4QD5Z1ePipe5L2xJpBSZa-Dpeh_Gt3viqmNgxUjlbnPHEcJNU_0XNk5WNVFmaQxNf8KM7AgAErv9CZbp2EEO2t5odgz5IyctVPTf3hS-tf3BRlqN-C1wJFt3Pp5VXMftIOh8yYNQTV1oOKgUBKcnhtHmAIV-qlyvE-stKsgNRWFLdkaIUUIM1gQzMkdLwQsxEowDa9FYLmfBRxUqrf7RBfDQwClK76Xwh0qlQVgOt1JplQ3WGD3klvLthCkfy.ogJzy-WcIAwnKytpL7nFNoz1n4bqb7BmRCBLrvB9fo8%26version%3DPublished&cb=63861632096&encodeFailures=1&width=642&height=641&action=Access" height="100%" width="100%" alt="Bouncing Ball Game Steps"/>
</p>
<br />
<br />
<h3 align="center">Create the ball:</h3>  <br/>
<p align="center">
<img src="https://eastus1-mediap.svc.ms/transform/thumbnail?provider=spo&farmid=194112&inputFormat=png&cs=MDAwMDAwMDAtMDAwMC0wMDAwLTAwMDAtMDAwMDQ4MTcxMGE0fFNQTw&docid=https%3A%2F%2Fmy.microsoftpersonalcontent.com%2F_api%2Fv2.0%2Fdrives%2Fb!6V-MtG_eY0-k9L3oLFYG78uFi7wejWlDtk1uGQBckp1A2A3GGZExRqpoc3ruqnky%2Fitems%2F016IFZ7YIKTYWBCEWIXFE3KYGBNPA4ZD3M%3Ftempauth%3Dv1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwNTYwMDAifQ.9bnAgvYtBl9f_9zdDTd5sqKAYLy7_d1OCPlP0YyNp-N440V9wCmZHivH4w5-0xKkU44qHUlk-Lk1ayz74y82Sf0b3A8UxGfFkKmEJTM9BwUWRE4o-C_g1G2DU4THGWo4aclKyQzXygC-sK1mWvuirFWqycfc6oa-yT0q4_UwvfVZYInRMEZAKShjlCWTBBvHjTnJjhL8L-PeZJVcfkaDcJIVS9eMbhOHAxAaMQryqEEquBzHHaAQaKRyfw6k7W02dtdgjyjQCBU7jrH2WZeEo_fmKYjaOwwAmUbCs_Bkaqn9eUDKjaAFxHURAEIEw-zhY9rBOOJbjSP0Reyjrx3yF_igt_n5UoScnqOvzvw8oPDSmtXGb4OvQs2MbHwrlttz.EpKbfJcMlYfUsovZEdxaCLkCenJm87s8FPH4sXe7EAk%26version%3DPublished&cb=63861632109&encodeFailures=1&width=852&height=793" height="80%" width="80%" alt="Bouncing Ball Game Steps"/>
</p>
<br />
<br />
<h3 align="center">Add motion to the ball:</h3> <br/>
<p align="center">
<img src="https://my.microsoftpersonalcontent.com/personal/9917556fd42654bc/_layouts/15/download.aspx?UniqueId=e034da47-73b9-4b65-812b-cabc61f5b597&Translate=false&tempauth=v1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwMzkwOTAifQ.UIlYKHP01Ko4EqF68KtddRycUtOt5zowBdx45Lg06kVosMA9oN7phP63CWNVsgWaqkfhjAefRxKaSC2KIs8zZq8RKf6Cu63XSFGY-Vaa2FyaX_0Fp_MFYHwQHpP5aY6hABILd9d9BaBrmhpc8NSGBLKI21gk1V4p8txacG5dUrUWeSu2xczZpDYM96rG6G_I7RAJw-NlUJs2DlVtaFKXZcTmSgkCyFjNbGibk7PV3dQdlOpbfByA-nQ8kj2L00ZOQNsnJJc86VKzL4FEhpA_wQgdu_bzEDuemGt9RbMlmrM8ZHHvyCHQxEsdauaQvMrAsaAJMx-SWOUsrtwfuP5We6c8kmcGBd-fe7yRGfCiZ7CQBZdGv76y2bY1m9CTKto5Ar4915GGQNLQoZp5fCSp95ZspOjjCEByOj3XLmU1lG0.pPKtQyFnNuW0KrjgWSMaHlFPM5zAzcOPENcuYYHJiL8&ApiVersion=2.0" height="100%" width="100%" alt="Bouncing Ball Game Steps"/>
</p>
<br />
<br />
<h3 align="center">Add collision to the ball:</h3> <br/>
<p align="center">
<img src="https://my.microsoftpersonalcontent.com/personal/9917556fd42654bc/_layouts/15/download.aspx?UniqueId=36b27fab-8f9c-4195-ac83-893019bb962f&Translate=false&tempauth=v1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwMzkwOTAifQ.TBTQhpHOcLDzd6gtDqrbwUAYSUJNo5Sqrtjfrx5KnQV1Po9AEfcxshJQ0r1SzPcymDOasWkA8xG9_l6uh2lKs_fpnI5RklDnr-dhonABm5COgA943Jq1Eei1qHpIqDBwk7xL0Uih1xl0f2FbOOKLk6YrHcwOVYrb1BvgW2b3K48wNF9RjW-4dGEcE-GL7Wsz1UsEYZx8twS1Hsczar6-bxUIS0FifHUDf9o-u_nYYmXrTO4lbfstYUK2xbl9uyMDpMRrhlvOqugFBYL9PniX4AKuKpi2ZHZsJWsCerxWzp5yJBsxm8dG8cA7LBva4ZxLrjakwYST-DBTKPVblzRC3-LdFzCWHCSxeAMlq3l0izlws-t2Vnb0oxdUZL704I0zz5ezGlwLNsx61fNMJLXG3jFzlfZR-c7GumC4ryCIcNI.W2y5x10n_Axu2bOQ65c1p40O-LEg0hFJ3Kk71zntDQc&ApiVersion=2.0" height="100%" width="100%" alt="Bouncing Ball Game Steps"/>
</p>
<br />
<br />
<h3 align="center">Create the paddle:</h3>  <br/>
<p align="center">
<img src="https://eastus1-mediap.svc.ms/transform/thumbnail?provider=spo&farmid=194112&inputFormat=png&cs=MDAwMDAwMDAtMDAwMC0wMDAwLTAwMDAtMDAwMDQ4MTcxMGE0fFNQTw&docid=https%3A%2F%2Fmy.microsoftpersonalcontent.com%2F_api%2Fv2.0%2Fdrives%2Fb!6V-MtG_eY0-k9L3oLFYG78uFi7wejWlDtk1uGQBckp1A2A3GGZExRqpoc3ruqnky%2Fitems%2F016IFZ7YKND3PCKJHQ5ND3REPTTPLC3RPI%3Ftempauth%3Dv1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwNTYwMDAifQ.zlDVAEpD_vGJSARUKtgdCS0JCbLD1ilDwnScVMOfZJ1dZ1CBd-yl3j123QP3YEiGhzNY9uqGJIOni05zZ-5kd8zprwSphco5yBy5ZczytKpoyoP7Xc7uD_mpdzIJQJYP5mhnBojAUzm9Vza9hR3eyCee1-3xpDZkJfdUnpviC3CcT2Tea41RCl8C6hu9-LKK8DOyWOoci6xxkI9BNqWH9Vi0lx9CszZafkd9-eeFqJPhC3BcsW4llRPs1rdfbiMogxONt_WQi07ngmaGhcUAuL1XVSfRBSDW0VaLZWXQiJXHdtARGB4L_IS1AIsEdnNpakKWtHUMQgjdQ4xwWp2SpfFfEPhKhMtGbkjRmrRwATOJClqevlhp113spTtilkwE.W1xsQVEY6bR65xTQhZLfbVQKATxP9BrPDVKbpkNUwq8%26version%3DPublished&cb=63861632160&encodeFailures=1&width=494&height=429" height="100%" width="100%" alt="Bouncing Ball Game Steps"/>
</p>
<br />
<br />
<h3 align="center">Add motion to the paddle:</h3>  <br/>
<p align="center">
<img src="https://my.microsoftpersonalcontent.com/personal/9917556fd42654bc/_layouts/15/download.aspx?UniqueId=253f33ce-1378-42f2-809a-80f73d9372fa&Translate=false&tempauth=v1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwMzkwOTAifQ.J8e1MljPpaeWmuuJY7nD3xJ7r8HaUaFIFZBZB2l-GZokY4GTZkjndxDQ_j_fLdE7bbI7Ar7lAdNkFvQ25CuYN7_9x1PaP7wa6hrzH5qnV8z5l8zhA_gmdEBeS7sAA8RXCtHvwxBW6ZyZd03DFa0DIviE81MA0JoAXX-PJpet2spsuMDuxZXitWVmWrKVwy_QdqK7X1BEb_Q4vLnb6QEWHEYKoG3aXNz6pT4aKSNfUutVUWR3UD0bYyrRzWB7D4FU20k0zWnc1oueHXi0t9OIC7Bbzil0e8YF2ZvMfTj7DGT0-FF-w8ZzFig8YTXc_ecx7f9ID8Xq88TBSR6MlAGoFJabEed-7CP4CY4KBRw1KZDcNZHbvNLyOGg8OeUUSPJg_c0s9sEADG1-FH1Qh7gH0Wa3kXEaXN6wTnE578xXdzM.BCryWMXbc0imtOdbSzVy31Uv_EQ88WqlGE3YRdypde4&ApiVersion=2.0" height="100%" width="100%" alt="Bouncing Ball Game Steps"/>
</p>
<br />
<br />
<h3 align="center">Add collision to the paddle:</h3>  <br/>
<p align="center">
<img src="https://my.microsoftpersonalcontent.com/personal/9917556fd42654bc/_layouts/15/download.aspx?UniqueId=3d7af9b0-0b4d-4451-b82e-824f12a3ea3d&Translate=false&tempauth=v1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwMzkwOTAifQ.MSBs8rfs-Z_QD8YsN7KwXIGmMws_DrADC34XhxZO2arDe_L-K0bWLHwltwV3Q66088lTUZt56MP2qRd9sDgd_ehFs4KmGfoFdCBK0UJBZ8f7RgsibGfNvso6WUvu2RY2xzYCBj8QXBGYPJSeSYHbnouseRp81Ysgi-6mYbCaKR2mSQazFfYb4qWO3qP5St0_REY5pQv3-aC1LElt1BpzUFjSj4EDjZfbWlHDwYEeQPWZY_wf0LbMAbrBV9QJsl3frqc57DxRsPCwGabwW4_pQG2m3hSRYrmypv5kWcGTSEBVC5_C--VUklUmxUwT08nk5H9lhWV9oaOEIpdG_90U_tVB3Q-ew4Bd2Q4dWnzIOaokSIbRHLLs-jGc72wWFK00f-oYKJjIkjUFHcCBDG8_Koz2x28oF2zUtHRRSmsn7_Q.4hCEFKQoL4HXweD_xiRaD92PoVeOL_dv6ItHeAkW_X8&ApiVersion=2.0" height="100%" width="100%" alt="Bouncing Ball Game Steps"/>
</p>
<br />
<br />
<h3 align="center">Add an element of chance to the game:</h3>  <br/>
<p align="center">
<img src="https://my.microsoftpersonalcontent.com/personal/9917556fd42654bc/_layouts/15/download.aspx?UniqueId=7e27f70c-45f6-43ca-826a-7cc406969b01&Translate=false&tempauth=v1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwMzkwOTAifQ.RjDSdF2sw-4COnbvFpWy_LXXhlkX3yQa9Pq60e4NDpCnV_bRdm33imCIJfJQky_r2cVidbhgpJesEDHK3ppYWSbMab3sdKFfIrJ91SydsoAxNRl0yNX-R07tJDaCff3OmWrbTtR7Esp6sA_rGMA2yKwMsSMeCnviSjqwStDk2UngoNY86ic0YSWSZOpap7Mh6iGV_gkaHTTlUXjYO8yFJj5zyqZcD8NPcO6WyxypvkMm1HSwugXK7Gpz_NHI3luJDOPUcn4Y_RJpdcbflCAvwE5RSJ7O7ZY3tWri3wmK2wBfPs0cpob9dVOfXVQ7ayfkEY4TYapCRE_zP_75iuU5ivzeahQHVyrRzjGpKbCEuCJTPw8C8NA81XDnqecWMjnS8MuVQHmysIdwf3ANs2xWPN33S9J6SVfJ8YT8Zq_-drU.nLN9Em9Lwr0Lq_UtRDLys2HLFGwPBiHp-fwRt__IW_k&ApiVersion=2.0" height="100%" width="100%" alt="Bouncing Ball Game Steps"/>
</p>
<br />
<br />
<h3 align="center">Final touches! Randomizer, delayed click to start, ball aceleration, score, color changes, & game over:</h3>  <br/>
<p align="center">
<img src="https://my.microsoftpersonalcontent.com/personal/9917556fd42654bc/_layouts/15/download.aspx?UniqueId=d968897f-99d8-4e2b-9847-30f7c42334ef&Translate=false&tempauth=v1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwMzkwOTAifQ.3nx9t49_G5kU0IZyYUJSsCS7OWTm5LYEnNuoQDe-gIw33HhRosYhUBw_aWKacXSfTuvITb0Lb7HvZq7mmaXA03-r31hIfX3_CIObbJlv1rOhkKI_mzAZsubSD883jJpDoZBpCg419qv95leQthW-lz4OggoBOQ90_uPVbsNVXM3o-jPRSJ8POjr1HVow13baj04GoyTgEGz-LNnjJI_JFTcai1UqJvzsVfpZ3Caa6ETlXGvBuRrUG_gR0hiEvsUrk25D9i8DVbrSibqhLkbLQdrxoczdIpV5-9s67J-LMey_iBHRbrYGpD0BZ4JYH_Ca5PksaPdU6-w4TBbTY-oDErPbkNK9lOmw7y_y87a6RSeDaWptH6FDLstWWRuJ358mHP4mJddcxjz2MjFIJG7YutPdXpIgd8eXOYtesrH49m8.MO36j-CjJiq8Xvl2MxNAA4zlORX3uoZ5Kb0BlbPFtbc&ApiVersion=2.0" height="100%" width="100%" alt="Bouncing Ball Game Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
