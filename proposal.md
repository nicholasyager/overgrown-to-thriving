---
theme: gaia
backgroundColor: #fff
marp: true
---

<!--
This video should be 2-5 minutes long. Your pitch does not need to be refined! Tell us the main idea behind your session, key topics that you plan to cover, and what audience members will learn. Feel free to share your screen if you want to use a doc or slides to run through your session at a high level. We recommend using Loom
--->

<!-- _class: lead -->

# From Overgrown to **Thriving**

Scaling Your dbt Project Like a Gardener

---

<!-- _class: left -->

<style scoped>
    small { color: gray; font-weight: thin; margin: 0; }

    section:where(.left) {
        display: flex;
        flex-flow: column nowrap;
        justify-content: center;
    }

</style>

<h1>Nicholas Yager</h1>
<small>they/them</small>

Principal Analytics Engineer
Hubspot

![bg right 75%](assets/profile_pic.png)

<!-- footer: 'Coalesce 2023 Pitch'  -->

---

![bg](https://www.asergeev.com/pictures/archives/2012/1071/jpeg/11.jpg)

<!-- _footer: ''  -->

---

![bg](assets/graph.png)

<!-- _footer: ''  -->

---

![bg contain](assets/graph.svg)

<!-- _footer: ''  -->

---

<!-- _class: lead -->

# <!--fit--> dbt deployments can be tricky to scale

---

# <!--fit--> dbt deployments can be tricky to scale

1. Large organizations tend toward decentralization

<!-- Suppose you're in an organization of ~ 4,000 employees. Based on dbt Lab's reporting that organizations tend to resource their data teams with 1-2% of headcount, we should expect there to be ~40 - 80 people in the data organization. If we're conservative and estimate that maybe a quarter of those people work within the organization's dbt project, we're looking at 10 - 20 full time dbt contributors. Following the two-pizza rule of team sizes, it would be reasonable to expect there to be 2 to 4 distinct operating teams working within the project. -->

---

# <!--fit--> dbt deployments can be tricky to scale

1. Large organizations tend toward decentralization
2. Decentralization can lead to inconsistent standards and design principles

<!--
Once you're in territory where there are multiple distinct teams forming, storming, norming, and performing, it's common for there to be drift in how the teams operate. This can be something as trivial as leading commas vs trailing commas. It can also, however, become something as important as the definition of a Customer. Perhaps GTM analytics defines a customer as a CRM account with subscription, whereas a finance analytics team may define a customer as a corporate entity. This definition mismatch means that these two analytics teams now have entirely incompatible customer reporting.
-->

---

# <!--fit--> dbt deployments can be tricky to scale

1. Large organizations tend toward decentralization
2. Decentralization can lead to inconsistent standards and design principles
3. It's so easy to add "just one more" model

<!-- And now we're in the endgame of how to resolve our differences. Do we put in the effort to have GTM align with Finance or vis versa, or do we make just a few more models that shim together bits of both to workaround the reporting difference? dbt makes it delightfully easy to reference existing models and start pulling in data from somewhere else in the project. -->

---

<!-- _class: lead -->

# This leads to **sprawl**

---

# Survey your garden

1. What are your core entities?
2. What are your exposures?
3. How are your data consumers using your models?
4. Are there any obvious architectural issues?
5. Are there any anti-patterns being used?

---

# Clear out the weeds and trash

1. Remove deprecated or otherwise unused models
2. Consolidate duplicate models

---

<!-- _footer: ''  -->

![bg 75%](https://hips.hearstapps.com/hmg-prod/images/hankscorpioflamethrower-1528493255.gif)

---

<!-- _class: lead -->

# Renewal pruning

---

![bg 70%](https://bugwoodcloud.org/images/1536x1024/5377064.jpg)

<!--
Gradual removal of unproductive branches to allow a plant to spend its resources growing healthy branches.
-->

---

![bg contain 90%](https://mermaid.ink/svg/pako:eNqNVcGOmzAQ_RXL1aqX7CqwUbrl0EtzbC_tESJkzJDQGhvZZrer1f57DYZgiAPLJR7mvTdvZpDzhqnIAUe4YOKFnonU6MevhCccmYcyotQBCqREIymgomQs-rTfZk_hfoOUluIvjDEVTMghnAlUpgjr-dvt1132OPKHuOfbcMbn8PLTkciCfZEFo8QQ9xI2nEnUsnwmGlyZoihWbVgVpV8ZIPhHqppB6KO7bU_QgQ-dkd2XMGvVLaNjNdlJkvp8KRN_l2AcGxI5lfxkh6hQISTSZ-iXoo6jQl5KoLoUvNshch6LfYztbxocoyiyZx9uN-BCFzdFdmbCuBtni-rimZj1nXapNIiVPqWugWGpS6zQZYULLNsgur__Nq_r7dADDBfddwTb9KJfLw54Pt311bKD-CD4Z43-iJIPm0XmSPpJH6dF1zYdfHDT4Uc3vbxoW3Ns3VvKl54M5u4OUVk95ECYmrnuU7RRWlQgPelairyh-gGegWt11YxBtB9Sj0rTC8wxZDCNAnkr1_KNiTQdDN5IuyanED9RQi2kvlgTjaaG7uCup9N_va4f_5ymwMtrR3M6twt-NqjZGMeyHWFq4LrcHLS0kg7rrGG58o3ZrXlZozn11_F4g41wRcrc_I2-te8SbO7nChIcmWMOBWmYTnDC3w2UNFr8fuUUR1o2sMFNnZs7_lAScx1UOCpMZ_D-HyRHatc)

<!-- https://mermaid.live/edit#pako:eNqNVcGOmzAQ_RXL1aqX7CqwUbrl0EtzbC_tESJkzJDQGhvZZrer1f57DYZgiAPLJR7mvTdvZpDzhqnIAUe4YOKFnonU6MevhCccmYcyotQBCqREIymgomQs-rTfZk_hfoOUluIvjDEVTMghnAlUpgjr-dvt1132OPKHuOfbcMbn8PLTkciCfZEFo8QQ9xI2nEnUsnwmGlyZoihWbVgVpV8ZIPhHqppB6KO7bU_QgQ-dkd2XMGvVLaNjNdlJkvp8KRN_l2AcGxI5lfxkh6hQISTSZ-iXoo6jQl5KoLoUvNshch6LfYztbxocoyiyZx9uN-BCFzdFdmbCuBtni-rimZj1nXapNIiVPqWugWGpS6zQZYULLNsgur__Nq_r7dADDBfddwTb9KJfLw54Pt311bKD-CD4Z43-iJIPm0XmSPpJH6dF1zYdfHDT4Uc3vbxoW3Ns3VvKl54M5u4OUVk95ECYmrnuU7RRWlQgPelairyh-gGegWt11YxBtB9Sj0rTC8wxZDCNAnkr1_KNiTQdDN5IuyanED9RQi2kvlgTjaaG7uCup9N_va4f_5ymwMtrR3M6twt-NqjZGMeyHWFq4LrcHLS0kg7rrGG58o3ZrXlZozn11_F4g41wRcrc_I2-te8SbO7nChIcmWMOBWmYTnDC3w2UNFr8fuUUR1o2sMFNnZs7_lAScx1UOCpMZ_D-HyRHatc -->

![bg contain 79%](https://mermaid.ink/svg/pako:eNqNVctymzAU_RWNOplunIyxKXFYdFMv202zDBlGiItNAhKjR9xMJv9eGfMQWJbDSuI87tHRGH9gynPAMS4qfqB7IhT6_TdhCUPmoRWRcgsFklwLCqgoqyr-Fi2zzSpaIKkEf4VxT3nFRb-dGdRmSNXpl8uHMFuP-n7f6U_bswgMDn8skyyIiiwYTfp9Z3LaziwaUb4RBbZNURRfDCLVewUI_pG6qWDlktsHn7ADFzsj4f0q691bjc52gjT7YcjTLwEmLyLoUOYg-hK5QGoPqCZNU7Ld82iQlwKoKjlrrxBZT6v8Ecdxu3BgkQd7MFjfvgO-90g3I-YKhG5vf3YzXMYT2BVsJER-eDPCwPKj2eXag6ctZ98VEvDCS9ZW_UhqQFuiiAQln6ejrpQeeNpZe9tZeZShVxmMB1-7jP2wpQ796vCs1ePy5gZRUd_lQCppYp4-HROIaql4DcIBN4Lnmqo7eAOmbHxgSLVLO1aaDjSrKMPREsQl7Kg3IdK0D3gBtkNOKW6hgIYLNUTjWlEjl_OLsttpm5zmcfc0JQ6vLc9pbwN_VtSsxnFsK5gGOB83J_mupOVa1-CffKG7a1muyaz51_l4gY1xTcrc_Bl-HN8l2Pz2a0hwbJY5FERXKsEJ-zRUohV_fGcUx0poWGDd5OZLvS2J-ZTUOC7MyeDzP4kNRXw)

<!-- https://mermaid.live/edit#pako:eNqFVU1vmzAY_iuWp2qXtAoJoymHXZbjemmPpULGvCRsxka2aVZV_e9zCB-GOoaTzfPxPn6skA9MRQ44xgUTJ3okUqPfTwlPODIPZUSpPRRIiUZSQEXJWPwtWme7TbRCSkvxF8Y9FUzIfjszqMwQ1unX64cw2476ft_pL9uZnsPp0bLIgqjIgtGi33cWl-3MopblG9Fg2xRFsRjj4qL0OwME_0hVM9i45PaxJ-zAxc5IeL_JevdW02QHSerjMOTllwSTFxF0KnOQfYVCIn0EVJG6LvnhdTTISwlUl4K3F4isp1X-iOO4XTiwyIM9GKxv3wHfe6S7EXMFQre3P7sZLuMJ7Ao2EiI_vBth4PnZ7Hrtwcte8O8aSfgjSt5W_UwqQHuiiQKtXqejFkoPPO1sve1sPMrQqwzGg29dxn7YUod-dfil1fPy5gZRWd3lQJgyMS8fjglEG6VFBdIB11LkDdV38AZc2_jAUPqQdqw0HWhWUYbTKJDXsLPehEjTPuAV2A45pbiFEmoh9RBNNJoauZpflN1O2-Q0j7unKXF4bXlOexv4s6JmNY5jW8E0wNdxc5LvSlqudQ3-yVe6W8qyJLPmL_PxChvjipS5-Sv8OL9LsPntV5Dg2CxzKEjDdIIT_mmopNHi-Z1THGvZwAo3dW6-1PuSmE9JhePCnAw-_wPVd0Sy -->

![bg contain 83%](https://mermaid.ink/svg/pako:eNqFVUtvnDAQ_iuWq6iXTbTsUtJwiFRpj-2lPYYIGXvYpTE2sk3SVZT_XsPyMMQLnDx8jxm-kcw7ppIBjnHO5Rs9EWXQz9-JSASyD-VE6wPkSMtaUUB5wXn8Jdpm33fRBmmj5AuMNZVcqr6cGZS2Ce_02-1DmO1HfV93-ks50wt4--VYZEGUZ8Fo0dedxaWcWVSqeCUGXJs8z1fHuLhoc-aA4B8pKw47n9z97Ak78LEzEt7vst691dTZUZHqNDR5-sEYKgutC3G0FsCZRkQwO59SQE0XqdUU4nm0YUUDFlK0a0TO0_K_xXHcHjxYtIA9WKzfgQe-H6W-puj29rHz8YknsK_5SIhGGARr2NcTDJ4OUnw16K8sBDInQAwqKwJBz0jmiDj187TrSojBQlD7xSR2C8pwURmMGex9xsvwfoTDZXX4KeDmeHODqCrvGBCu7ZiX62AC0VobWYLywJWSrKbmDl5BGBcfGNoc046VpgPNCcpyag3qGtbo7RBp2g94BXaHnFL8QgWVVGYYTdaGWrmeL8pNp01yOo8_pylxeO14TnMb-LOgZjGObVvBdIDP7eakpZW0XGcNy52vZLc2y5rM6b_OxxtsjUtSMPuDe2_eJdheBCUkOLZHBjmpuUlwIj4sldRG_jkLimOjatjgumL2f3EoiL1VShzn9svg4z-bOjw3)

<!-- https://mermaid.live/edit#pako:eNqFVUtvnDAQ_iuWq6iXTbTsUtJwiFRpj-2lPYYIGXvYpTE2sk3SVZT_XsPyMMQLnDx8jxm-kcw7ppIBjnHO5Rs9EWXQz9-JSASyD-VE6wPkSMtaUUB5wXn8Jdpm33fRBmmj5AuMNZVcqr6cGZS2Ce_02-1DmO1HfV93-ks50wt4--VYZEGUZ8Fo0dedxaWcWVSqeCUGXJs8z1fHuLhoc-aA4B8pKw47n9z97Ak78LEzEt7vst691dTZUZHqNDR5-sEYKgutC3G0FsCZRkQwO59SQE0XqdUU4nm0YUUDFlK0a0TO0_K_xXHcHjxYtIA9WKzfgQe-H6W-puj29rHz8YknsK_5SIhGGARr2NcTDJ4OUnw16K8sBDInQAwqKwJBz0jmiDj187TrSojBQlD7xSR2C8pwURmMGex9xsvwfoTDZXX4KeDmeHODqCrvGBCu7ZiX62AC0VobWYLywJWSrKbmDl5BGBcfGNoc046VpgPNCcpyag3qGtbo7RBp2g94BXaHnFL8QgWVVGYYTdaGWrmeL8pNp01yOo8_pylxeO14TnMb-LOgZjGObVvBdIDP7eakpZW0XGcNy52vZLc2y5rM6b_OxxtsjUtSMPuDe2_eJdheBCUkOLZHBjmpuUlwIj4sldRG_jkLimOjatjgumL2f3EoiL1VShzn9svg4z-bOjw3 -->

![bg contains 65%](https://mermaid.ink/svg/pako:eNqVlk9vmzAYxr-KxVTtklaBJGzjsMty3C7bMVTImJeEFmxkm3ZV1e8-gyEYx4GFSzD-PY_ffwl59wjLwIu8vGSv5IS5RD9_xzSmSF2kxELsIUeCNZwAyouyjD6F6_RrEK6QkJw9w7gmrGR8WFoGlTqk7PXr9bdtuhn1w7rX66Wlp_D6y7BI_TBP_dFiWPcWemlZ1Lx4wRJMmzzPF8PQLkK-lYDgL67qEgKX3Ex7QvsuOsXbL0HaumtFp2rSI8f16XzM4QcHFbES4WNBj7qIAuWMI3mCvinicXRor6zgQGTBaNdHc0fz24P-TLaPURTpexe3G7jdPBcOXGhyFqkTSLoEEhWBPCaabDXd0znB7lZBaAmG6bHj6uhgdHTWC93ff7cz6J5ptbN2Ds1uQRM6NKFTAzSbDs7F5PiHPaOfJXpiBR3GBBVUMlQC7r-Mt86NP_TZn5-HYOCCeW4zcJv_nRv_1jEI3ALHDBy68bhmqvN39Md3FsABBguZjX2ezecqpivq2p4My90dIrx6yACXwmpOv0UaIVkF3LFdc5Y1RD7AC1ApLnqmiLbaPZUkZ8wISDGNAH5tr9WrIJJkCPDKthnkFHELOdSMy3NorJFEyYU9EWZ1-h6a8bjrNAXPjw3Pad3OvFUoq4zjsZ1gGsDlcTY015KONdowf_KV2i3FsiQzzl_mvZWnjCtcZOp_ynv7LPbUC7CC2IvUbQY5bkoZezH9UChuJPvzRokXSd7AymvqTL1E9wVWP5GVF-UqM_j4BzLN2KY)

<!-- https://mermaid.live/edit#pako:eNqVlk9vmzAYxr-KxVTtklaBJGzjsMty3C7bMVTImJeEFmxkm3ZV1e8-gyEYx4GFSzD-PY_ffwl59wjLwIu8vGSv5IS5RD9_xzSmSF2kxELsIUeCNZwAyouyjD6F6_RrEK6QkJw9w7gmrGR8WFoGlTqk7PXr9bdtuhn1w7rX66Wlp_D6y7BI_TBP_dFiWPcWemlZ1Lx4wRJMmzzPF8PQLkK-lYDgL67qEgKX3Ex7QvsuOsXbL0HaumtFp2rSI8f16XzM4QcHFbES4WNBj7qIAuWMI3mCvinicXRor6zgQGTBaNdHc0fz24P-TLaPURTpexe3G7jdPBcOXGhyFqkTSLoEEhWBPCaabDXd0znB7lZBaAmG6bHj6uhgdHTWC93ff7cz6J5ptbN2Ds1uQRM6NKFTAzSbDs7F5PiHPaOfJXpiBR3GBBVUMlQC7r-Mt86NP_TZn5-HYOCCeW4zcJv_nRv_1jEI3ALHDBy68bhmqvN39Md3FsABBguZjX2ezecqpivq2p4My90dIrx6yACXwmpOv0UaIVkF3LFdc5Y1RD7AC1ApLnqmiLbaPZUkZ8wISDGNAH5tr9WrIJJkCPDKthnkFHELOdSMy3NorJFEyYU9EWZ1-h6a8bjrNAXPjw3Pad3OvFUoq4zjsZ1gGsDlcTY015KONdowf_KV2i3FsiQzzl_mvZWnjCtcZOp_ynv7LPbUC7CC2IvUbQY5bkoZezH9UChuJPvzRokXSd7AymvqTL1E9wVWP5GVF-UqM_j4BzLN2KY -->

<!--
In a dbt project, we can prune our project by refactoring any anti-patterns currently in use in the project's core entities. This would include
-->

---

<!-- _class: lead -->

# Divide the perennials

<!--
Dividing the perennials is the notion that we ought to separate your most industrious plants to prevent overcrowding and to allow for specialized treatment of plants in the garden.
-->

---

![bg](https://www.gardening-guy.com/wp-content/uploads/2012/07/Dividing-hostas-005.jpg)

<!-- _footer: ''  -->

<!-- This is a picture of hostas being split up! -->

---

# <!-- fit -->Groups and Access

```yml
groups:
  - name: go_to_market
    owner:
      email: gtm@garden.supplies

models:
  - name: deals
    group: go_to_market
    access: public
```

![bg right 90% vertical](https://mermaid.ink/svg/pako:eNqFU01vgzAM_SsovbZVtU3VlsNOPW6X7YqE0uC0aIEgx-k0Vf3vS6FAmgHjhO33YT_BmUmTA-NMafMtjwIpeftIq7RK_CO1sHYHKrHGoYREFVrzxXazf37YLhNLaL5gqKXRBvlCKRWxS--gb-TN5uVp_ziQuzokR_Qai5MgeA9UPGxSoi2vKr0SluschLac8_aSoS-dJVMCxrMaTe4kreEEFYXDdmzpkN0gWdZjmkNbgLOAo4Mr0xtnWbfR2CzcKpiPUBBqg9TvYhxJTwxAUQTJavUa7TASxj2qb3dq9-H04CiQMKvBrUEHvn9dYsRk4g0wCHrGcCKm2RVmOYHt_2C2ZF61FEXuf7TztZcyOkIJKeP-NQclnKaUpdXFQ4Uj8_lTScYJHSyZq3P_-e8KcUBRMq78TXD5BcffSEs)
![bg right 90% vertical](https://mermaid.ink/svg/pako:eNqNlMtugzAQRX8FOVsSRW0VtV50lWW7abdIyJhxgmpj5EeqKMq_1wkYOw4oZYXHZ-6dB-KEqKwBYcS4_KV7okz28VW0RZu5h3Ki9RZYpqVVFDLWcI4Xm3X1-rTJM22U_IFwppJLhReMsSRbOAc-JK_Xby_Vc0j25zg5Se9UcyAGPiMVh81K9Eevos2Rg5OQtaVmKruqqphUcIDWwj9IarWRAlSpLaWg9WzK0I4SqxoI1xjjfpwh7qXSu6Hs1aUmE18Oddhqp0i391wf7SvclUOwLMfseJCBtdr1MDIiXEJb3zkN47l1ci2Upe9t2mTE4lanUS_0oJJ0_EFAQSeVGfuX1lAHzkuOm8mWy_ekoYkd3VJj2Kvd7myEk22EzzN2u9KR771LSgQuMbiC0Wq9YfCZGVOPRZmPYZQjV5sgTe3-I6dLrEBmDwIKhN1rDYxYbgpUtGeHEmvk97GlCBtlIUe2q91HsG2I26tAmLn64PwHdwiO4g)

<!--
Just like a garden needs to be divided into separate areas for different plants, a dbt project can be modularized into smaller sections. In this section I'll discuss some basic philosophies around how to identify which models should be grouped together, how to consolidate similar models, and how to leverage groups and access controls to manage dependencies between sections.

https://mermaid.live/edit#pako:eNqNlMtuwjAQRX8lMltAqK1Q60VXLNtNu41kOc4YEHYc-UGFEP9el8SxMYloVvH4zL3ziHJGTNWAMOJC_bAd1bb4-Cqbsin8wwQ1ZgO8MMppBgXfC4Fn61X1-rSeF8ZqdYB4ZkoojWec8yxbegfRJ69Wby_Vc0wO5zQ5S2_1_kgtfCYqHpuU6I5BxdiTAC-hasfsWHZVVSm5VcQqIqk-wH9w5oxVEjQxjjEwZjKl70nLZQ1UGIxxN9MYD1L5XV_7Eo7Q2PSyr8NVW03bXeC6aFfhlvRBQobsdJqRdcb3MDAyXkJT3zmlM7q1830QEhocdxqwtN9xNAg9KCffQRTQ0CpthyEoZ5kHpyWH9RSLxXvW0MiibqkhHNRuFzfA2Urih5q6XenE994lJyKXGVzBZL_BMPpMjKnDkszHMJojX5uk-9r_Uc5_sRLZHUgoEfavNXDqhC1R2Vw8Sp1V36eGIWy1gzlybe0_gs2e-r1KhLmvDy6_ykSS5A

https://mermaid.live/edit#pako:eNqNlMtugzAQRX8FOVsSRW0VtV50lWW7abdIyJhxgmpj5EeqKMq_1wkYOw4oZYXHZ-6dB-KEqKwBYcS4_KV7okz28VW0RZu5h3Ki9RZYpqVVFDLWcI4Xm3X1-rTJM22U_IFwppJLhReMsSRbOAc-JK_Xby_Vc0j25zg5Se9UcyAGPiMVh81K9Eevos2Rg5OQtaVmKruqqphUcIDWwj9IarWRAlSpLaWg9WzK0I4SqxoI1xjjfpwh7qXSu6Hs1aUmE18Oddhqp0i391wf7SvclUOwLMfseJCBtdr1MDIiXEJb3zkN47l1ci2Upe9t2mTE4lanUS_0oJJ0_EFAQSeVGfuX1lAHzkuOm8mWy_ekoYkd3VJj2Kvd7myEk22EzzN2u9KR771LSgQuMbiC0Wq9YfCZGVOPRZmPYZQjV5sgTe3-I6dLrEBmDwIKhN1rDYxYbgpUtGeHEmvk97GlCBtlIUe2q91HsG2I26tAmLn64PwHdwiO4g

-->

---

# Multi-Project Deployments

![bg contain 75%](https://mermaid.ink/svg/pako:eNqVVE1vgjAY_iukXtWYuRjWw04mu8zLtiMJKe2LkhVK-qEzxv--IpQWlCyDC337fPVtywVRwQBhlHNxogcidfT-kVRJFdmHcqLUFvJICSMpRHnBOZ5tVln8tJlHSkvxDX5MBRcSz_I8H7FL68A78mr18pytPdmNQ_KIXsviSDTsAhULm5Roh05F6TOH6O1r55iseT05jmM3WJwKpg84Wtc_Q3YtBTNU_1PB8yUcoTLwKHuWZSGSGqVFCTJVhlJQapJyI_UpTbaXpD64oG21ebrCsgmgFca43UgPUHqfdqA07VFhxz3WKBusx5R-Eip2F8V2vGNSWS4ZED62b-puvQ-jOamufX7GBbcKaeqkH2ceQEO3abgTLIdTwSIH6cZbNhSTUAup-xYLo6kFT8kPffqL4BoYLRavo4U_aOUQ1Zed2vBI9ODRIfAXIHS7oQPfe5cxwuNGBjdgcKKcofeZaF0LC5h_g9Ec2WwlKZj9z12aWoL0AUpIELafDHJiuE5QUl0tlBgtPs8VRVhLA3NkamYPyrYgdr9LhHObD66_ple6gQ)

---

<!-- _class: lead -->

### New tooling will be created for this

### purpose over the next few months.

---

<!-- _class: lead -->

# Keep the weeds under control

<!--
Now that we've gotten our garden into a more maintainable state state, it's
vital that we prevent weeds and other unwanted plants from taking root. In a garden
this can take a great deal of time and effort. Thankfully, this is where our
metaphor breaks down in our favor.
-->

---

![bg](https://longislandweekly.com/wp-content/uploads/2015/07/iStock_000013798533Large.jpg)

<!-- _footer: ''  -->

---

<!-- _class: lead -->

<!--
Instead of manual effort, we can use fantastic tools to keep our garden
productive. For a while, we've had tools like pre-commit and sqlfmt to keep our
queries readable and maintainable. As of last year, we've also had developments in
architectural monitoring tools like dbt-project-evaluator and Whetstone to monitor and report on _what_ we've built as well.
-->

| Surface Area            | Tools                                                                        |
| :---------------------- | :--------------------------------------------------------------------------- |
| Coding Conventions      | sqlfluff <br /> sqlfmt                                                       |
| Documentation & Testing | dbt-checkpoint <br />dbt Core tests and contracts                            |
| Modeling                | dbt_project_evaluator <br /> Whetstone                                       |
| Data Quality            | dbt*expectations <br />Great Expectations<br />Data Fold <br /> \_Many* more |

---

<!-- _class: lead -->

# Take a short break

and then grow a bright future

<!--
We've come a long way! Our project now has fewer unused models, a more efficient
structure, clearly-delineated responsibilities, and automated guardrails to keep
new growth in check. We can now take a small break and enjoy our handy work.

When we're ready, we can continue to deliberately cultivate our garden with confidence and clarity.
--->

---

<!-- _class: lead -->

# From Overgrown to **Thriving**

#### Scaling Your dbt Project Like a Gardener

Nicholas A. Yager
yager@nicholasyager.com
