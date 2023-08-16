---
theme: mdsFest
marp: true
---

<!--
This video should be 2-5 minutes long. Your pitch does not need to be refined! Tell us the main idea behind your session, key topics that you plan to cover, and what audience members will learn. Feel free to share your screen if you want to use a doc or slides to run through your session at a high level. We recommend using Loom
--->

<!-- _class: lead -->

# From Overgrown to **Thriving**

Scaling Your dbt Project Like a Gardener

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

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
<p>
Principal Analytics Engineer
<br />
<small style="color: #D8621D;">HubSpot</small>
</p>

![bg right 75%](assets/profile_pic.png)

---

![bg 103%](https://www.publicdomainpictures.net/pictures/200000/velka/verwilderter-hinterhof.jpg)

<!--
![bg](https://www.asergeev.com/pictures/archives/2012/1071/jpeg/11.jpg) -->

<!-- _footer: ''  -->

---

![bg](assets/graph.png)

<!-- _footer: ''  -->

---

<!-- _class: lead -->

# dbt projects can be tricky to scale

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

---

# dbt projects can be tricky to scale

1. Large organizations tend toward decentralization

<!-- Suppose you're in an organization of ~ 4,000 employees. Based on dbt Lab's reporting that organizations tend to resource their data teams with 1-2% of headcount, we should expect there to be ~40 - 80 people in the data organization. If we're conservative and estimate that maybe a quarter of those people work within the organization's dbt project, we're looking at 10 - 20 full time dbt contributors. Following the two-pizza rule of team sizes, it would be reasonable to expect there to be 2 to 4 distinct operating teams working within the project. -->

---

# dbt projects can be tricky to scale

1. Large organizations tend toward decentralization
2. Decentralization can lead to inconsistent standards and significant overhead

<!--
Once you're in territory where there are multiple distinct teams forming, storming, norming, and performing, it's common for there to be drift in how the teams operate. This can be something as trivial as leading commas vs trailing commas. It can also, however, become something as important as the definition of a Customer. Perhaps GTM analytics defines a customer as a CRM account with subscription, whereas a finance analytics team may define a customer as a corporate entity. This definition mismatch means that these two analytics teams now have entirely incompatible customer reporting.
-->

---

# dbt projects can be tricky to scale

1. Large organizations tend toward decentralization
2. Decentralization can lead to inconsistent standards and significant overhead
3. It's so easy to add "just one more" model

<!-- And now we're in the endgame of how to resolve our differences. Do we put in the effort to have GTM align with Finance or vis versa, or do we make just a few more models that shim together bits of both to workaround the reporting difference? dbt makes it delightfully easy to reference existing models and start pulling in data from somewhere else in the project. -->

---

<!-- _class: lead -->

# This leads to **sprawl**

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

---

![bg 103%](https://www.publicdomainpictures.net/pictures/200000/velka/verwilderter-hinterhof.jpg)

---

![bg](https://c2.staticflickr.com/4/3092/5809787537_7d926fca26_b.jpg)

---

# Step One: Survey your garden

<!-- _class: lead -->

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

---

# Survey your garden

1. What are your core entities?
2. What are your exposures?
3. How are your data consumers using your models?
4. Are there any obvious architectural issues?

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

---

<!-- _class: lead -->

# Step Two: Clear out the weeds and trash

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

<!--
1. Remove deprecated or otherwise unused models
2. Consolidate duplicate models -->

---

<!-- _footer: ''  -->

![bg 75%](https://hips.hearstapps.com/hmg-prod/images/hankscorpioflamethrower-1528493255.gif)

---

<!-- _class: lead -->

# Step Three: Renewal pruning

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

---

![bg 70%](https://bugwoodcloud.org/images/1536x1024/5377064.jpg)

<!--
Gradual removal of unproductive branches to allow a plant to spend its resources growing healthy branches.
-->
<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

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
<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

---

<!-- It's dangerous to go alone! Take these. -->

![bg 90%](assets/dbt_project_evaluator.png)

---

![bg center 90%](assets/whetstone.png)

---

<!-- _class: lead -->

# Step Four: Divide the perennials

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

---

![bg](https://www.gardening-guy.com/wp-content/uploads/2012/07/Dividing-hostas-005.jpg)

<!--
Dividing the perennials is the notion that we ought to separate your most industrious plants to prevent overcrowding and to allow for specialized treatment of plants in the garden.
-->

<!-- This is a picture of hostas being split up! -->

---

<!-- _class: lead -->

## Groups and Access

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

---

![bg 90%](https://mermaid.ink/svg/pako:eNqFU01vgzAM_SsovbZVtU3VlsNOPW6X7YqE0uC0aIEgx-k0Vf3vS6FAmgHjhO33YT_BmUmTA-NMafMtjwIpeftIq7RK_CO1sHYHKrHGoYREFVrzxXazf37YLhNLaL5gqKXRBvlCKRWxS--gb-TN5uVp_ziQuzokR_Qai5MgeA9UPGxSoi2vKr0SluschLac8_aSoS-dJVMCxrMaTe4kreEEFYXDdmzpkN0gWdZjmkNbgLOAo4Mr0xtnWbfR2CzcKpiPUBBqg9TvYhxJTwxAUQTJavUa7TASxj2qb3dq9-H04CiQMKvBrUEHvn9dYsRk4g0wCHrGcCKm2RVmOYHt_2C2ZF61FEXuf7TztZcyOkIJKeP-NQclnKaUpdXFQ4Uj8_lTScYJHSyZq3P_-e8KcUBRMq78TXD5BcffSEs)

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

---

```yml
groups:
  - name: go_to_market
    owner:
      email: gtm@garden.supplies

  - name: customer_success
    owner:
      email: customer_success@garden.supplies
```

```yml
models:
  - name: deals
    group: go_to_market
    access: public

  - name: report_product_outcomes
    group: customer_success
    access: public
```

---

![bg 90%](https://mermaid.ink/svg/pako:eNqNlD1vwyAQhv-KRdYkstoqahk6ZWyXdrVkYXwkVsFYfKSKovz3ktgYQuImTOZ47n3vOOQDorIGhBHj8pduiTLZx1fRFm3mFuVE6zWwTEurKGSs4RzPVnn1-rSaZ9oo-QNhTyWXCs8YY0m2cA58SM7zt5fqOST7fZycpHeq2REDn5EKO688n9Tpt15Kmz0HpyNrS82kRFVVMa5gB62FR3FqtZECVKktpaD1_3lDi0osayBcY4z7Kw5xr5eeDV0sT9WZ-HAoxlYbRbqt5_poX-amHIJlOWbHlxtYq10jIyPCIbT1ldNwUZdOroWy9L3dNhmxuNXbqBe6U0k6gyCgoJPKjP1La6gDpyXHyWSLxXvS0I0ZXVJj2KtdzmyEk2mE1xq7nenI99olJQKXGJzBaLTeMPhMXFOPRZn3YTRHrjZBmtr9Ww6nWIHMFgQUCLvPGhix3BSoaI8OJdbI731LETbKwhzZrnaPYN0QN1eBMHP1wfEPyLKVKg)

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

<!--
Just like a garden needs to be divided into separate areas for different plants, a dbt project can be modularized into smaller sections. In this section I'll discuss some basic philosophies around how to identify which models should be grouped together, how to consolidate similar models, and how to leverage groups and access controls to manage dependencies between sections.
-->

---

![bg 90%](https://mermaid.ink/svg/pako:eNqNlEtOwzAQhq8SmW2LIh4VeMGKJWzoNlLkOGMa4cSRH0VV1TOwYcdFOA8X4AqYJn7UfUBW8fib_5_xOFkjKmpAGDEuXumCSJ09PBVd0WX2oZwodQ8sU8JIChlrOMdns7y6uZhNMqWleIGwpoILic8YY0l2ax34mJznt1fVZUh26zg5Se9lsyQaHiMVtn3y_KjOsHRSSq84WB1RG6qPSlRVFeMSltAZ-C9OjdKiBVkqQykodTpvbFG25zUQrjDGwxGHuNNL98Yuzn-r0_HmWIypniXpF44bokOZz-UYLEufHR9uYI2yjXimDZvQ1XtO40HtOtkWytL1dtjEY3Grh1En9Ecl6QyCgIReSO37F0ZTCyaSEeiVFqTvm85qHXX3Q8ym07uk9wPj3KV82KntjtfDyeDCxY7dtnTku--SEoFLDLZgdAucYfA5cqIDFmWehk8UWqCvj_fvz7cCRQr7c3EavOle5tsv8cZ_anA1g-tbR6AJspktaWr7u1v_xgqkF9BCgbB9rYERw3WBim5jUWK0mK86irCWBibI9LW9l_cNsVetRZjZc4DND55Xyqg)

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

<!--
Just like a garden needs to be divided into separate areas for different plants, a dbt project can be modularized into smaller sections. In this section I'll discuss some basic philosophies around how to identify which models should be grouped together, how to consolidate similar models, and how to leverage groups and access controls to manage dependencies between sections.
-->

---

## Multi-project deployments

⚠️ Caution: Prickly practice 🌵

<!-- _class: lead -->

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

---

![bg contain 75%](https://mermaid.ink/svg/pako:eNqVVE1vgyAY_iuGXdvGrEvjOOzUZJf1su1oYhBfqhmK4aNd0_S_j7YiaOuWcZKX54sX8IioKABhxLjY05JIHb29p03aRHZQTpRaA4uUMJJCxCrO8cMqzpPH1SxSWoov8HMquJD4gTE2YtfWgXfkOH5-ypee7OYheURvZbUjGjaBCruMOJ7UuU6dlNIHDtHr52aSniSJm8z3VaFLHC3b7yG_laIwVP9bwytI2EFjYFIhz_MQTo3SogaZKUMpKPU778LsE5t8K0lbutDX6nl0hcU5ilYY4-vZeoDS26wDZVmPCg_BY42y6XpM7RehKW6i2P53TCrrRQGEj-3Pdbfpu9GcVNdIv-KCW4Usc9L3Mw-gods03AnWw6Vgk4N043MbiklohdR9i4XR1IKn5Ic-_dtwDYzm85fRxu-0cojqy05teCV68OgS-McQul3Qge-tyxjhcSODCzC4Uc7Q-0y07goLmH-D0QzZbDWpCvvrO55rKdIl1JAibD8LYMRwnaK0OVkoMVp8HBqKsJYGZsi0hb0o64rY864RZjYfnH4AXLHAAw)

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

<!--
1. Teams have more flexibility and self-determination
2. Clear lines of ownership and responsibility for all models.
3. Public interfaces between projects can be versioned and contracted
 -->

---

![bg 90%](assets/github_discussion.png)
![bg 90%](assets/multiproject_dbt_cloud_2.png)

---

![bg 90%](https://mermaid.ink/svg/pako:eNqFUl1PwyAU_SsEX6vpWu02Hkz8ejDRuKiJidYYWi4bSqHhQ53L_rvQbk6NHzzA5XDu4dwLC1xrBphgLvVLPaPGobPLUpUKhVFLau0xcFRJWj8hLqQkW7wbaZog64x-ArKVxk2tpTZd_D03pE6N9oqtBTKeQcX5HwLfJFojnqmD8-BU_uFivFvln3Tidi1l3VwCur6YrNJPTg6L7OCLg55qfTU1tJ1F7h2rHDqS2rP7XoUJA7UTWqHrwxVSuQfjlRMN9GxtAF32wD0hZFN8z2-NDsWAo2b-0Eo_FepusoHQeVgYdRRNurOfFJiwtX6GkE9bsXGIDian9l8-2t7e_8HDb946-qcSUSTCSjlOwftj6Ei8tvshkR-bHNcbamCmvYX1aX8LTnADpqGChU-3iFiJ3QwaKDEJIQNOvXQlLtUyUKl3-mquakw4lRYS7NvQHzgWNLxS84G2VGGywK-YDHdGRZGno2yQZaM0G-YJnmMyKAY7Rbo3ynfHRTrOh3vLBL9pHQQGXfJtFzvjYfkOXQYB2g)

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

---

![bg 90%](https://mermaid.ink/svg/pako:eNqNUm1r2zAQ_itC_eoWx16dVB8GbcOg0LGwFUoXj6JIp1itLBm9bMtC8tsr2c5SRgvTB-nu9Dz33J20xcxwwAQLZX6xhlqPbr_WutYoLqaoc3MQaKUoe0ZCKkVORL_yPEPOW_MM5CRPDjPK2N7-lxupa2uC5ocEhShgJcT_Jmgk56BH8tXl_Lr8dKQe_JE9uGP9zm8UoLsvi3e4vVRCurBaW9o1Cbt8MMGiGy0sjbjAfLDwY6iISwvMS6PR3dUYWflHG7SXLSyjja5NBBNCjj0PuM6azkrw1G4eOxXWUi8XxxD6HA9OPUWL_i5lGJo-6DpmfkLk0k4OOsoEji4XN-419g002u_3b6i_V1UPf9UUSkAYu0hbrPopziC12H-J09OP_YDTeU8tNCY4ONwOKjjDLdiWSh5_2TbFauwbaKHGJJocBA3K17jWuwilwZtvG80wEVQ5yHDo4mRgLml8ofZvtKMaky3-jcn0bFZVZT4rJkUxy4tpmeENJpNqclbl57Pyw0WVX5TT812G_xgTE0x68vfeju8LuxfhXv3x)

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

---

![bg 90%](https://mermaid.ink/svg/pako:eNqNUm1P2zAQ_iuW-RpQmkBa_GESUCEhbaIaSIg1E3Ltc-Ph2JFftnVV-9uxk3RsE0jzh-Tu_Dx3z915i5nhgAkWyvxgDbUeffxc61qjeJiizs1BoJWi7BkJqRQ5Ev3J8ww5b80zkKM8OcwoY3v7X26krq0Jmh8SFKKAlRD_m6CRnIMeyZcX86vy-pV68Ef24I76nd8oQPe3i3e4famEdGG1trRrEnb5aIJFN1pYGnGB-WDh66CISwvMS6PR_eUYWfknG7SXLSyjja5MBBNCXnsecJ01nZXgqd08dSqspV7edrGnu1iLAfoUbzj1FC36u7cycOmY-Q6RTzs51FImcHSxuHEJPwzpsLi_0Gi_37-h4D1l6Pj4w5-NoQSEUUf6LKz5FueQRPbPIuHTkNP_gVpoTHBwuB2q4Ay3YFsqeXxp2xSrsW-ghRqTaHIQNChf41rvIpQGb-42mmEiqHKQ4dDF6cBc0ril9ne0oxqTLf6JyfRkVlVlPismRTHLi2mZ4Q0mk2pyUuVns_L0vMrPy-nZLsO_jIkJJj35S2_HHcPuBdQu_kU)

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

---

![bg 90%](https://mermaid.ink/svg/pako:eNqNU1FP2zAQ_iuWeQ0oTUda_IAEVEhITK1WJLQlqHKcS-Ph2JFjb-uq_vfZTjrYyND84Nydv-_uvvi8x0yVgAmuhPrOaqoNuv-Uy1wit5igXbeAChWCsmdUcSHISRVWHEeoM1o9AzmJvcOUUDrYf3MddauVleUxQVIlUFTV_yaoeVmCHMjXV4ub6e0L9egP7N4d-u_MTgB6WK7-wQ2lPLKzxVbTtvbY7LOyGt3JSlOHs8xYDU99RyXXwAxXEj1cD5HCbLSVhjeQORvdKAcmhLxo7nGtVq3mYKjebVpht1xmy9ZpWrtaDNBHd1JSQ9EqnI1l6HenA7rsXjEq0K23x6Cq-Ora3HRGabqFbBlctO7dMULJO6a-geuNtrzXIZQt0dXq7k2BEQY6Pb0cUfiq43cRf7b7LvRtPMBf3UL4TzAI89tKK5_eqwgz7PF-Ivz3kWqole3geNpXwRFuQDeUl-5Z7H0sx6aGBnJMnFlCRa0wOc7lwUGpNWq9kwyTiooOImxbd5Ww4NSNVPM72lKJyR7_wGR2Nk_TaTxPJkkyj5PZNMI7TCbp5CyNz-fTDxdpfDGdnR8i_FMpl2ASyF-C7QYSDr8AEEs6uA)

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

---

![bg 90%](assets/loom.png)

---

![bg contain 75%](https://mermaid.ink/svg/pako:eNqVVE1vgyAY_iuGXdvGrEvjOOzUZJf1su1oYhBfqhmK4aNd0_S_j7YiaOuWcZKX54sX8IioKABhxLjY05JIHb29p03aRHZQTpRaA4uUMJJCxCrO8cMqzpPH1SxSWoov8HMquJD4gTE2YtfWgXfkOH5-ypee7OYheURvZbUjGjaBCruMOJ7UuU6dlNIHDtHr52aSniSJm8z3VaFLHC3b7yG_laIwVP9bwytI2EFjYFIhz_MQTo3SogaZKUMpKPU778LsE5t8K0lbutDX6nl0hcU5ilYY4-vZeoDS26wDZVmPCg_BY42y6XpM7RehKW6i2P53TCrrRQGEj-3Pdbfpu9GcVNdIv-KCW4Usc9L3Mw-gods03AnWw6Vgk4N043MbiklohdR9i4XR1IKn5Ic-_dtwDYzm85fRxu-0cojqy05teCV68OgS-McQul3Qge-tyxjhcSODCzC4Uc7Q-0y07goLmH-D0QzZbDWpCvvrO55rKdIl1JAibD8LYMRwnaK0OVkoMVp8HBqKsJYGZsi0hb0o64rY864RZjYfnH4AXLHAAw)

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

<!--
1. Teams have more flexibility and self-determination
2. Clear lines of ownership and responsibility for all models.
3. Public interfaces between projects can be versioned and contracted
 -->

---

<!-- _class: lead -->

# Step Five: Keep the weeds under control

<!--
Now that we've gotten our garden into a more maintainable state state, it's
vital that we prevent weeds and other unwanted plants from taking root. In a garden
this can take a great deal of time and effort. Thankfully, this is where our
metaphor breaks down in our favor.
-->

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

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

<h2>
Your <strong>process</strong> is more
important than your tools
</h2>

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

---

# Ways to keep the weeds under control

1. **Perform code reviews for every change, and make reviews easy!**

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

---

# Ways to keep the weeds under control

1. **Perform code reviews for every change, and make reviews easy!**
   - Show your DAG changes
   - Use CI/CD and dbt tests
   - Pick your SQL syntax and enforce it using SQL formatters.

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

---

# Ways to keep the weeds under control

1. Perform code reviews for every change, and make reviews easy!
2. **Review your project's architecture often**

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

---

# Ways to keep the weeds under control

1. Perform code reviews for every change, and make reviews easy!
2. **Review your project's architecture often**
   - Use an architecture evaluation tool like dbt_project_evaluator or Whetstone
   - Look at your DAG. Really!

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

---

# Ways to keep the weeds under control

1. Perform code reviews for every change, and make reviews easy!
2. Review your project's architecture often
3. **Periodically check to see if the execution behavior of your project has changed**

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

---

# Ways to keep the weeds under control

1. Perform code reviews for every change, and make reviews easy!
2. Review your project's architecture often
3. **Periodically check to see if the execution behavior of your project has changed**
   - Track materialization run times (dbt_artifacts or dbt Cloud) to find bottlenecks in your project
   - Leverage query usage data to identify unused models

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

---

![bg](https://upload.wikimedia.org/wikipedia/commons/thumb/a/ac/Jardin_en_permaculture.jpg/1200px-Jardin_en_permaculture.jpg)

---

<!-- _class: lead -->

# Take a short break

and then grow a bright future

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>

<!--
We've come a long way! Our project now has fewer unused models, a more efficient
structure, clearly-delineated responsibilities, and automated guardrails to keep
new growth in check. We can now take a small break and enjoy our handy work.

When we're ready, we can continue to deliberately cultivate our garden with confidence and clarity.
--->

---

<!-- _class: lead -->

<video autoplay="" playsinline="" loop="" muted="" style="margin: 0 auto; width: 5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>

Nicholas A. Yager
yager@nicholasyager.com

<div class="footer">
  <div class="logo">
  <video autoplay="" playsinline="" loop="" muted="" style="width: 1.5em;">
    <source src="assets/mds-wave.mp4" type="video/mp4">
  </video>
  <span>
  MDS FEST
  </span>
  </div>

  <div class="small_title">
  From Overgrown to Thriving
  </div>

  <div></div>
</div>
