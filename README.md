<div align="center" id="toc">
<ul style="list-style: none">
<summary>
 <h1>Bouncing Ball Game</h1>
</summary>
</ul>
</div>
 
<br>
 
<h2>Description</h2>
This project is a game that utilizes the 'tkinter' module within Python to create a bouncing ball and a controllable paddle. To begin playing the game, the player clicks anywhere in the game window. The ball bounces around the screen and the paddle is used to prevent the ball from hitting the bottom of the screen which will cause a GAME OVER. A score counter is located at the top right and it rises each time the ball hits the paddle. To add a bit of difficulty the ball will increase in speed if the paddle is moving in the same direction once it strikes the ball. If the paddle was struck while moving in the opposite direction of the ball, the speed of the ball will decrease.
<br />
<br />
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
<br /><br />

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
<img src="https://eastus1-mediap.svc.ms/transform/thumbnail?provider=spo&farmid=194112&inputFormat=gif&cs=fFNQTw&docid=https%3A%2F%2Fmy.microsoftpersonalcontent.com%2F_api%2Fv2.0%2Fdrives%2Fb!6V-MtG_eY0-k9L3oLFYG78uFi7wejWlDtk1uGQBckp1A2A3GGZExRqpoc3ruqnky%2Fitems%2F016IFZ7YKH3I2OBOLTMVFYCK6KXRQ7LNMX%3Ftempauth%3Dv1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhdWQiOiIwMDAwMDAwMy0wMDAwLTBmZjEtY2UwMC0wMDAwMDAwMDAwMDAvbXkubWljcm9zb2Z0cGVyc29uYWxjb250ZW50LmNvbUA5MTg4MDQwZC02YzY3LTRjNWItYjExMi0zNmEzMDRiNjZkYWQiLCJleHAiOiIxNzI2MDU2MDAwIn0.vcQQPGrd--mlVf8WDDEVj5nLQ33EeTTlJVRIu59BqgC8pnnMmMmy38_tYVmToxhNAgOZb17IyX3qZdz9hsXc0c1AvcADwtVpeD1Akk-tXL2iWrpCeM6ehuBH7dM14p7YLyLoID6YKZyLKhHWduFEjzFJJIm0p4f-bM1tejodzCXRIw0mb9iaEuZbhjQRtKBgwQgmH0dzq4loxcNe2PS9lCMCCKzOswsQSuC2d47BxkfKwatQgp8NO7dT2jQbu7BYijKkDyK_iruqJA8HQHXISjzBlMPGlfpS9SofliZ4OAjxsjp01Dri58Ii3vyzbn-xE2AfEvEfhgZCsWyQqMya8At8mJTbR-k9h1rTwEJuQCbxor5-caKHNlJbzOUNF7Vm-3j3svFDeCELPHyoEpa59MWDr-5lUdw2fILJFFK-F2varytFRz3Y8vdL9D6CVI8Blc95WRp2cpGnluv4Z4Apb-jiHYA541I9Yc9YttFw2Fzq15Ye3Dd6WidfEX10O_8V.YV7ciuJ9ks5mrv3uBf6t6ihQHpEY1P0-NuX7tGlLS8A%26version%3DPublished&width=1024&height=999999&cb=63861632124" width="100%" alt="Bouncing Ball Game Steps"/>
</p>
<br />
<br />
<h3 align="center">Add collision to the ball:</h3> <br/>
<p align="center">
<img src="https://eastus1-mediap.svc.ms/transform/thumbnail?provider=spo&farmid=194112&inputFormat=gif&cs=fFNQTw&docid=https%3A%2F%2Fmy.microsoftpersonalcontent.com%2F_api%2Fv2.0%2Fdrives%2Fb!6V-MtG_eY0-k9L3oLFYG78uFi7wejWlDtk1uGQBckp1A2A3GGZExRqpoc3ruqnky%2Fitems%2F016IFZ7YNLP6ZDNHEPSVA2ZA4JGAM3XFRP%3Ftempauth%3Dv1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhdWQiOiIwMDAwMDAwMy0wMDAwLTBmZjEtY2UwMC0wMDAwMDAwMDAwMDAvbXkubWljcm9zb2Z0cGVyc29uYWxjb250ZW50LmNvbUA5MTg4MDQwZC02YzY3LTRjNWItYjExMi0zNmEzMDRiNjZkYWQiLCJleHAiOiIxNzI2MDU2MDAwIn0.ZmyuQqRtRO5FUupkOoduWvrXl4ouAoNYBxpPAhnIcZYPUwnJJMA2rUtBzn9kY7YDSu-89yL42Ly2mjY84xVygQdzfYtnDfHKLahen3AlGYApRFBm9oJrOa2Om-VVdMFDl-f1agYA3TkXvQhvcgFgRr6LCGAOZkn2xCTiPABT26ZCiaYODIl8RUFjNcesid2bIh38qKV1TrRhvXRGSAhwM2BI-mxT_pKp85_2Jc8bfSUx19UdB_o8DsKK893xDp6zPCThlR_NF3KVuKDsu_pfToTNIu7jS-1I0bFa1JrxTpBexWCuMoXO4tS8QSMhNfaJ9FP_3dVQNJNC_hNcr9bWqu_k4mcL4NDdDXuu9p_oX0fJug3eSD_5MqKJfbRO3arE9UQTs7pIfJCD4hCHiE7NuDOhnuEKyNx4tjEXcIBcmTKVd6eYFrg9vTex3E0q26aTpc-oSCUXxCmwQ1hv0SLtMUP6LyKgl7rbU9-bvT7v2vBk_fGtKCY90AgRjXH0UzEp.XsF-KgE0E0QVBVs9-0tvGWT55EHQ7Fo-JpIXlM2gGWo%26version%3DPublished&width=1024&height=999999&cb=63861632144" width="100%" alt="Bouncing Ball Game Steps"/>
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
<img src="https://eastus1-mediap.svc.ms/transform/thumbnail?provider=spo&farmid=194112&inputFormat=gif&cs=fFNQTw&docid=https%3A%2F%2Fmy.microsoftpersonalcontent.com%2F_api%2Fv2.0%2Fdrives%2Fb!6V-MtG_eY0-k9L3oLFYG78uFi7wejWlDtk1uGQBckp1A2A3GGZExRqpoc3ruqnky%2Fitems%2F016IFZ7YOOGM7SK6AT6JBIBGUA646ZG4X2%3Ftempauth%3Dv1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhdWQiOiIwMDAwMDAwMy0wMDAwLTBmZjEtY2UwMC0wMDAwMDAwMDAwMDAvbXkubWljcm9zb2Z0cGVyc29uYWxjb250ZW50LmNvbUA5MTg4MDQwZC02YzY3LTRjNWItYjExMi0zNmEzMDRiNjZkYWQiLCJleHAiOiIxNzI2MDU2MDAwIn0.TjzyXljyXix0X7-rzzb_n6lY497svslIduUc8T9vpblhdzUK65R5oGqwHf-w9yMYwTWqgniYfODt3OofwNpJTm-CChftGUcEl5Io7OWzv0xr25FZu4T2fHNy268JCetNs1Tbr3TdCVTDvAp7WdTVXljbvpPXLlT9D-MloR0kkZ810T01yFSBk19N0wMomoaBegLNuBrUGEBQlgNKxrMtvdpVx5vTp19ejnQqZR8pLWBQljef1Q8KoTU8Kscz_tywVTg3x12A8WlVOt5DqfjBo1nn6S4dU_31uCBwdUS2tB08a3qYsf7rsjqaV9DeRD7zvm9XLcthjGjDaEklGVpSKh2UClxqsYNIQttPFIQ40ZNWFsKZto45eL4u0NC6HUtvv0zPePxTyuBAhRANjySpPB0oHyppmPGwI39dpUIMM-rf8mnMrgROMsGaZYKoDflLdE-VyMjRJKgDgI8p2iQyEwlQoDzFoQBJE6uJYkB11nIBKU1BwcCnJi2MmLDMVqSc.fjUCUJ80BZtFQ4THpyQczGhYKEgkOl-jIZzEjylTrzA%26version%3DPublished&width=1024&height=999999&cb=63861632175" height="100%" width="100%" alt="Bouncing Ball Game Steps"/>
</p>
<br />
<br />
<h3 align="center">Add collision to the paddle:</h3>  <br/>
<p align="center">
<img src="https://eastus1-mediap.svc.ms/transform/thumbnail?provider=spo&farmid=194112&inputFormat=gif&cs=fFNQTw&docid=https%3A%2F%2Fmy.microsoftpersonalcontent.com%2F_api%2Fv2.0%2Fdrives%2Fb!6V-MtG_eY0-k9L3oLFYG78uFi7wejWlDtk1uGQBckp1A2A3GGZExRqpoc3ruqnky%2Fitems%2F016IFZ7YNQ7F5D2TILKFCLQLUCJ4JKH2R5%3Ftempauth%3Dv1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhdWQiOiIwMDAwMDAwMy0wMDAwLTBmZjEtY2UwMC0wMDAwMDAwMDAwMDAvbXkubWljcm9zb2Z0cGVyc29uYWxjb250ZW50LmNvbUA5MTg4MDQwZC02YzY3LTRjNWItYjExMi0zNmEzMDRiNjZkYWQiLCJleHAiOiIxNzI2MDU2MDAwIn0.8cOBeV6TBRGRL2MN0Y7Tet-U5FkVB_PA2iE76gghRZ-HFEiGgknlsaYifemDnoFvIlbAOwSmpWas_Wf5ScWBOmf2ur7U7IRV579KCXtnuWyKgfRMc5eKGwngDxgQseacePT3XNzBUOiVi6Rl3zRtH-1ggJY5m_tZTeMcTngGFhAhxoaA7YxHGCzs2zXoQqTETA9gfeXcX37ncZrDhFA-48jjoW8QVRsTy4k3uwMzkHkTSBEYu3Ifk0wKpowZnSPr3BkubKkoU78nV0TBVB8PCjPPINi8QOzEZwY-QzB9bjd0dR8WXmt9EJLIKcnwTaa0WmVxFjc1i-3r13pXExuL_SFjFTnNpsiQNSUBeTAb5ZV-s-aQU7Xuul7C-whCjZc0y0D5wgRR07xQFBkyjRzHzcBvvuMXQ19FE0KQMFTkv3STY3NXS-3EuQaLjvwfRozAXLW9nmyovl-GACd5A8p6xhSj5oZjxiC-REnyOwDrIiv6jrTBUuMAsct2m8rIcfGL.f5BN43TOXsdRKVZTCc79hTdjmVm3t4JfAovlfS6sxh4%26version%3DPublished&width=1024&height=999999&cb=63861632206" height="100%" width="100%" alt="Bouncing Ball Game Steps"/>
</p>
<br />
<br />
<h3 align="center">Add an element of chance to the game:</h3>  <br/>
<p align="center">
<img src="https://eastus1-mediap.svc.ms/transform/thumbnail?provider=spo&farmid=194112&inputFormat=gif&cs=fFNQTw&docid=https%3A%2F%2Fmy.microsoftpersonalcontent.com%2F_api%2Fv2.0%2Fdrives%2Fb!6V-MtG_eY0-k9L3oLFYG78uFi7wejWlDtk1uGQBckp1A2A3GGZExRqpoc3ruqnky%2Fitems%2F016IFZ7YIM64TX55SFZJBYE2T4YQDJNGYB%3Ftempauth%3Dv1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhdWQiOiIwMDAwMDAwMy0wMDAwLTBmZjEtY2UwMC0wMDAwMDAwMDAwMDAvbXkubWljcm9zb2Z0cGVyc29uYWxjb250ZW50LmNvbUA5MTg4MDQwZC02YzY3LTRjNWItYjExMi0zNmEzMDRiNjZkYWQiLCJleHAiOiIxNzI2MDU2MDAwIn0.1RpGzyw02SgEwxABRXvGko-5BLAQ6N8i5EvHet1-KI12iwgdHYDt-0aZyqyRaGbZFqSds5nM9amikrUu1vGof0TKSc6BozJNIyLbYJKjT_AiV74kLw01XuMBB-kLIavZtZRlDYvxG0uTWtLkztcD5C24mtOtzfL0Jy3Ar4nC1FUYAUiFfJwLOrgPOrUz3jOKFLGIvp8zqZSEZNL5pSUJ7__DWvgFeUaLbPmY3pfsp-vP8u3skaGck23R5psFrIVDeFniNvbncj3oScS-oVXBkyEX7oVDCd_FHNsbA86M1blsK0FSqX5pY8RpkpZDApGlwi_pebJ2o8XdHlmwteJB1Zy6sv2I2-L6c3GxX3JoospSAxD-VYFLi4EfVpJLRVxkhc4Om3bNY2QaavDww7EM8G9LB9CPrzYSqzuvlhNjhAzf3qXIePpFf0JAk2-TysnGRJ5wSgKtk6_vlHm8Oq2hw7LIKJCVOM_M1rJJCJxht-7Et77tk9VMmEIFwwyA-4nH.9OMKjcdDuJsYXXI4X9AUgsP0c00N9Om37o3aXCOMkr4%26version%3DPublished&width=1024&height=999999&cb=63861632220" height="100%" width="100%" alt="Bouncing Ball Game Steps"/>
</p>
<br />
<br />
<h3 align="center">Final touches! Randomizer, delayed click to start, ball aceleration, score, color changes, & game over:</h3>  <br/>
<p align="center">
<img src="https://eastus1-mediap.svc.ms/transform/thumbnail?provider=spo&farmid=194112&inputFormat=gif&cs=fFNQTw&docid=https%3A%2F%2Fmy.microsoftpersonalcontent.com%2F_api%2Fv2.0%2Fdrives%2Fb!6V-MtG_eY0-k9L3oLFYG78uFi7wejWlDtk1uGQBckp1A2A3GGZExRqpoc3ruqnky%2Fitems%2F016IFZ7YL7RFUNTWEZFNHJQRZQ67CCGNHP%3Ftempauth%3Dv1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhdWQiOiIwMDAwMDAwMy0wMDAwLTBmZjEtY2UwMC0wMDAwMDAwMDAwMDAvbXkubWljcm9zb2Z0cGVyc29uYWxjb250ZW50LmNvbUA5MTg4MDQwZC02YzY3LTRjNWItYjExMi0zNmEzMDRiNjZkYWQiLCJleHAiOiIxNzI2MDU2MDAwIn0.WGQ36kuV6tVBcmt-gHx1GKE2iUATL3Fvp-SUkLwqvtTQnHz3cWI__VGeIh9fxinUpFvoSIr5KIwZGBDG55BvQ2ldroxp18tFsSVf4A5yCkKGCU2XJRtnbT7LjN7Mm_q3k_-OwpzFb8UqK10XwJG7dUVSrFFQh90MFY9_EHGHxNGBv6T92rNVr6N4SoavenlR_LHNVbdIyKJdwDMn7pWgXrAWJMujvSxCF9hUAN0vUn443z6CcwHgQOxgdKk5igxKOHyManyfORRSQx8dXOJL-URc3xEFkI0yVS07wrtLEi0DNGbeIjiT0a187DfLkxhP53hh307TFPo7Emm_Z8zfo0a-SLeUNxZinVz0YotbuCNusLTpVzmBIUt3mQ_rNe4J6QahaanQgYm_cbPsL8_v3bNcI8NN5WPx_e7aFQFabrgUrXJR3BfFPQtFcU3HckS6camYYP27g6nc3ZG9vyQZWO8gT6TP3NWBo68GYy9PyTtEwBr28wmoou7YCdvgl1lu.p8ARsW3L61PRioUpba_fzlv-k3ntXIW3G9KxJXOm9t0%26version%3DPublished&width=1024&height=999999&cb=63861632231" alt="Bouncing Ball Game Steps"/>
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
