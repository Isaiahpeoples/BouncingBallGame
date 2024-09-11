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
<img src="https://my.microsoftpersonalcontent.com/personal/9917556fd42654bc/_layouts/15/download.aspx?UniqueId=e034da47-73b9-4b65-812b-cabc61f5b597&Translate=false&tempauth=v1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwNDUzMzUifQ.q4NUIKiTd9MyXVPq9tM9-ByeWgPw6mRkfuqUdFKN5t1OMTNe8s-O5nIfLi5xqVdrB7iUBfIhLlGB6OSNx4fHcyNwyyG1B0ulCZYA28fs308Bu9wRPLPE_edPU7IxDcrKDkwh2ijKyxAfh6B9mKukn54GEd7VouNBDrqZAnJaZzq1FzvFaMMu_NSAXXBH_pCsT7yUP_ZQ6tK5pyjt0QgDnPryOYiU08qXy_GWG0EY9GFg2viQVewUkRWsdD1nBIlMJRQX9AndUcLFa6ataKzXxeopFRboiru-NCK4GywhxRY3PQ5_6WiH_NYPDeJ-W6iHMSoWTiYWIwILVkNnPvvRsRhlrd-qiR-enNo0I3jGwLc9wCeoaRznmlrZXLpAMbYBeOammNbtH6JaMZbli1UB7t6Sss66YYXiWnkwt2tSLkE.B1bLHoReddoAV8ZxngxeZyK85KBDEqxDqNzffG5w_nI&ApiVersion=2.0" alt="Bouncing Ball Game Steps"/>
</p>
<br />
<br />
<h3 align="center">Add collision to the ball:</h3> <br/>
<p align="center">
<img src="https://my.microsoftpersonalcontent.com/personal/9917556fd42654bc/_layouts/15/download.aspx?UniqueId=36b27fab-8f9c-4195-ac83-893019bb962f&Translate=false&tempauth=v1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwNDUzMzUifQ.gueYfpcskhOPsB0kUk0KffY4i3QJtBZEresRCZZS-0HYNaVOEqMtC95mfRs4flZ0PR6KZUJn-1P5Mr7_xCohMNmNj-JKgJsqm3yFsPywXX43QDsEzLQ9IqEJ-2uL_fDzRL0mdylsd_7_eQlf8-0gq8uAOtAUEMRFCO6i3ogZTQcOjv2OBmFAoCdY0r34_GLEJVe3O-siZJp8VkboM7wlvofGH-b69Tn8E5sDEn7WbWKazD1lRG3AMQRfnPJuyhi1biUnbP0UC7hB0KoKs6_O0bzeGyVikLK33cfdAVXXQc3IM__B_WR3J8YSXmfdtnpq3wpKxhvfbf41hq4Z2Oq1lzWOzMWKji7Dsb5LBMnt36oxoYg3Q1leIopC-RcUiz8jdojzncNgC9yMd8jSxoyun7s9YxpL9hJSYsF_l-QfCkI.ECbZ21ttJ4NFkfiWQLSILFUb5Az9zXrOBfnn98xSqQY&ApiVersion=2.0" width="100%" alt="Bouncing Ball Game Steps"/>
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
<img src="https://my.microsoftpersonalcontent.com/personal/9917556fd42654bc/_layouts/15/download.aspx?UniqueId=253f33ce-1378-42f2-809a-80f73d9372fa&Translate=false&tempauth=v1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwNDUzMzUifQ.uYkzt6XvQjVN6W_R4BrfybdLu6hRUZgXL4RLw0csdgsvnDfIR_7BRBeinwAgvBUPWY9MSgNNBGeooJBzYm6hpUDbkWxBhIKMuohP2p4TOYXUeHKcMv8cQzgzcVHDwDWMl4Ca4ErmQYvIDDVDePY0gXNtSXpqfo8SWaktfQk2SLH-6fhniecs6AP8a58fOXdmq2NMbW6k5SRV18lXas7AGbqtklbefliXSrqmhAli2tvIj2uLaBKY4Cy5UsSBZ28pn4Na_bt1MgMFXiTI8Y6DIPXaYVDHV36Nm-So9jb3iccFGF0x-uNAuWiTRop44kFpbJeO5kPcdQEx9WT5qPdLAb8sG6Ll-fFQWJQoD0KYoVRg3iUlPk1FSuSqA049WuzZbpmST1EWxP71esw-FwJr1vnXvEA4GyPxEPTVnOElN9k.huDi_95qqqQXCaOwUekedZwW9JOmXng9lKOTFeYWdY8&ApiVersion=2.0" height="100%" width="100%" alt="Bouncing Ball Game Steps"/>
</p>
<br />
<br />
<h3 align="center">Add collision to the paddle:</h3>  <br/>
<p align="center">
<img src="https://my.microsoftpersonalcontent.com/personal/9917556fd42654bc/_layouts/15/download.aspx?UniqueId=3d7af9b0-0b4d-4451-b82e-824f12a3ea3d&Translate=false&tempauth=v1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwNDUzMzUifQ.0nIAEGmzyFDSUaYoDO0S0AyDvgHA5vhywG9_AkI0AZ0DEiErZFCLF01u4FOMKy3O7gNAmi1r1kGEGD86LFZRa8yVGEk15IaV6k-5gZejyvY4NBrRQrFEno6x5_KcEVvGObh1kRBDsvIZcpz6Z2J4bwDXZ3R9-FgvCgQT-k7DwwEsLardVlyCDI41vvXX7VK4Mq5ZYAqqgGA6guc-hY6ret3LjJH-RhJ5OhTXcakNZY9jQsLAONioCFLROhtigPvA_mqz2mue0cKaGKfdfoZKbnDQd8MYEIQueERTZXe0T8RWT2J3krln4ubnkX-zmJoMs2inPDLX_teJrW5zHT0WJN-rM1ytuNNOkpHc7BGWoJ-4oIhSm_wOXiQJsHRpQI6IHnfzMFRnUT2_YgRwb3SjPmqS3Vd6lkodBtvoZwEf8_M.U7tFJW27l1SdlqOneS-iQORIEx5TT0vwpgpTt0VRqKE&ApiVersion=2.0" height="100%" width="100%" alt="Bouncing Ball Game Steps"/>
</p>
<br />
<br />
<h3 align="center">Add an element of chance to the game:</h3>  <br/>
<p align="center">
<img src="https://my.microsoftpersonalcontent.com/personal/9917556fd42654bc/_layouts/15/download.aspx?UniqueId=7e27f70c-45f6-43ca-826a-7cc406969b01&Translate=false&tempauth=v1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwNDUzMzUifQ.b_vST1mRFHGooWKx-2iJwHDhFikXExqoDsGLHSBxzmkxUfFtPS_mwrsmyFaAVk3mSi3ZRa4g97R3-eIN2bQCTp-kcItC3aWmdtjWzNNsF-Fuf0FojAobdK9NpQwZxmufddX3H0juRnvKNzSpvWin8ki4dNFEXTCoP3dI-pR1DpLEhNrY6QvMBD4LF04Hj6EHQrPU4Zuti4IZkOo6393lymeTXdzXjLwHnw_fv8V16QTDW2u7lth6Jze8oD4cywj2rens5mrmhMly5o4JVBq5If-_iA5Ih6ghk1lCRRWC-yqKaeDtbVwI_FsNztr32oqnlUCnqxRteviM7DfFErQMx0r9MSvTcmZD5WBcyMGR2WaeR7hisq8YJCtN6sn65Nbpvx-TFq8-Up0RF3uENFAqQrL92TnaXXQcnWRy7SC8Y5s.GMuqcqeBrRuGcBBory13J1a6fT0ZgnnNRskYbaBnTjw&ApiVersion=2.0" alt="Bouncing Ball Game Steps"/>
</p>
<br />
<br />
<h3 align="center">Final touches! Randomizer, delayed click to start, ball aceleration, score, color changes, & game over:</h3>  <br/>
<p align="center">
<img src="https://my.microsoftpersonalcontent.com/personal/9917556fd42654bc/_layouts/15/download.aspx?UniqueId=d968897f-99d8-4e2b-9847-30f7c42334ef&Translate=false&tempauth=v1e.eyJzaXRlaWQiOiJiNDhjNWZlOS1kZTZmLTRmNjMtYTRmNC1iZGU4MmM1NjA2ZWYiLCJhcHBpZCI6IjAwMDAwMDAwLTAwMDAtMDAwMC0wMDAwLTAwMDA0ODE3MTBhNCIsImF1ZCI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMC9teS5taWNyb3NvZnRwZXJzb25hbGNvbnRlbnQuY29tQDkxODgwNDBkLTZjNjctNGM1Yi1iMTEyLTM2YTMwNGI2NmRhZCIsImV4cCI6IjE3MjYwNDUzMzUifQ.UDNpErHHdxNL7Nl9MlwJ8tpU1eeSrZUlSi7Iw_mzR0HFvd7r8qQ3ZB-UzkyoeRnd8woaxXIIYAgbES2vzbUSorcJzIXZJu3aSBoqQjZyWjdCGBvkDWP-fOPZ46sN7EvFWhnfpmD70vDifL7wIIqlaUztmNNiRyMNJ2Z-_guc6pMYy_puBSO6ffdYnJRQzEuRrzGmvA8-lKixSVfI4HesXRhA6OqQJBfGjIMwFj033ZCZIh5JF0BtiUnsVsGaJxJRAgaCryrjB-2Snv1j6xxL3ZVGEeEHbLjIN5-89SZIRkvfjWV9FV52z9vFvwm81PEn1YqAhuBA41ahLUCrV7hC0Zo9Y6BMhy-1JlPWi_Xg-Zpw78DIPSfJJ3Am_ZkuZ6Kd5YsoWIV1p-DAxtQuAP5e0gIjg7YkT5m4xfYoYCrmS8c.il7jfLWsYvD3RSZctKdvIed38MH0PlEzJwu4kMiEQk4&ApiVersion=2.0" alt="Bouncing Ball Game Steps"/>
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
