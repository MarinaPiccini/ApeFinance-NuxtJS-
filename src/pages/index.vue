<template>
  <div>
    <div class="big_div image_div hidden" style="padding-bottom: 200px">
      <div class="node_div logo">
        <NuxtLink to="/">
          <img src="../assets/icons/logo-text-big.svg" width="200" height="50" />
        </NuxtLink>
      </div>
      <div class="node_div">
        <div class="title">An avenue for</div>
        <div class="title">the evolution of <span class="defiText">DeFi</span></div>
        <div class="subtitle">Next-level liquidity. Friction-less yield. Light-speed swaps.</div>
        <div style="padding-top: 36px; position: relative">
          <Button size="large" ghost class="button_div" style="position: absolute; z-index: 999">
            <NuxtLink to="/swap/" style="display: inline-block; width: 100%; height: 100%">
              <div class="card-body" style="padding: 0; height: 100%">
                <div class="button_font">Launch app</div>
              </div>
            </NuxtLink>
          </Button>
          <div class="button_div_line button_div" style="display: inline-block; position: absolute; z-index: 999">
            <a
              href="https://raydium.gitbook.io/raydium/"
              target="_blank"
              style="display: inline-block; width: 100%; height: 100%"
            >
              <div class="" style="padding: 0; height: 100%">
                <div class="button_font">READ MORE</div>
              </div></a
            >
          </div>
        </div>
      </div>
    </div>
    <div
      id="animation_container"
      class="big_div image_div hidden"
      style="padding-bottom: 100px; display: flex; justify-content: center"
    >
      <a href="https://evm.apefinance.org/" target="_blank" class="card education">
        <div class="overlay"></div>
        <div class="circle">
          <svg
            version="1.2"
            baseProfile="tiny-ps"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 100 100"
            width="100"
            height="100"
          >
            <title>Background</title>
            <defs>
              <image
                id="img1"
                width="100"
                height="100"
                href="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGQAAABkCAYAAABw4pVUAAAAAXNSR0IB2cksfwAAE2VJREFUeJztXQl4FFW27iwEIjsoq8r+RBaXkWGGRZwRGUbkjYCKijIMM+rDZRwdPnXmOQKO8yQbYQlMEkggxJBA2AlrgBC2DATCnqT3LBBCEhYxLEm66553Tld36HRXdVc13amQ5Hzf/ymdqtt1z1/33HPuPee2StWIBEJUmxFDlH6OZlFZyBiFAMRGRKDSz9OkBQlohciwEnIXMUbpZ2rSggS8jqixEgIWciJUfko/V5MUCFX5IwH/sSODYEa8pPSzNUlBxU9xIMOG/Yi2Sj9fkxJUeF/EdRFCaJREIPyVfs4mIVZTtVCEDBsuI/op/axNQlDRgxDX3BBCWKD0szYJQUWvlkAG4RaZNqWft1ELmisaHZxEQgjxzW6wjwSVG2RdIpFKhm2U/FzpZ2+Ugor9M+KOTELAGqt0UPr5G5WgqeqMSs31gAyCCfF7pfvQqAQV+r8I5iEhhEuIdkr3o1EIKrITouQ+yLDhU6X70igEFTnHC2QQChAPK92fB1qADwLLvUQIIYW8NaX79UAK8Hsd67xIBuE2NO+ZeCaouElQd6/DW9gLYc3BoiyB+ZYFxNM+IINA3tp4pfv4QAkq7FW4PzfXHXaRSVS6nw+EoKLaIc75kAwCrYe9oXRfG7ygkshUfevj0WEDRf4Dle5zgxbwvpvrDhFK97lBCyootR7JINBi5WCl+90gBRUzFPjcqvokhLCcvDql+9+ghOICBUaHDT8hnlJaBw1KUCEvI6oVIoSQBqGqAKX10CAEFRGICvk/4PctlCKEVpN7Kq2LBiPAr1v9FXGznokg93ofNLu/zgIRFmKGAT+X+GINyxEG4LeFWyvd9wYlqJAWiGC7f1OkPgtx1YdkrAXeqwuwPYNyGmhggspoA/wm1EiHzx9GxHp5tFBG40SH76H6krn12+sGLqiQPggN4p+Ix8AaP+OET+7wS4gTIC8fyxE3EPPBmn1idbP7I75D5CN6K9j9hinAT+o0yR5DvGLvhuK/H0WsAmkppPagxOscxBu2hDkyUzRKgF/AZJbvnadYtxuuYLTcEu5VQ5GZSkQ8Wfv3MIsihyC2SxwtVxDvg11pAvBrZWvgXsxDHlbzlq6YoHKeBz5ytrmkOsRHSIa/3TWUo/UN4kcXoyLTMjfYRgWfMf8pQg/3VpJLoXk7172gkmaD8/J7GqKHw3VdrSPK/lqKY950uK6P9X779miENSfPSRE0XZTDu0fgzSdlf1vn2hBLlP+u1QTtQHSr/VuEZVTQCkCVQFu0Y9i0XF3YOfNxtmbUl1zmbNnlZVZbLxa1H7CYo9B7iQr47542s4b/T3PRaMQhkfvJJDatmnZu/yddIPrxYxDqz1j84EQu69tg93fVFeBdUrGdw0pEDKKjwz0dEUnAZ70L3UftzfFeTx8A4fJ+aM+ie+0gMixKCAs0QcLPlkH1NVmrqdbJW+wtt+E8YipN3vjftxAX3Fx/GJpSJjynTQlmicNjkYy6bml4y2q2ZvQC86XDckkZjqhwo2Tytra7MHE20FJM06kV4XLj27NVT22CUD/RGIH98Isoc9lxWZMp3vexG0VLxYe+6nuDEy43oQ3ED17rigzrSOFY0oh55kqj5DNJcPImr8vxgAC5yKJ9F1/qoMEId2pxEEv9bSjOFdKUE9HqNts4cYb56inppISoxgGfl+sJGeQANI3THbhjoS3Z6ue+hPAgeduvYS2q2JbX/8YV7pY0pwCfr0Urv3IXGOn6efaRfqMV0y1DAJqfcFKuR2/ugtaVLPU3kqNlvKcLUKK0vO/Zi6aq8W9AQWWJCpX5AYQF3N9EG9mmmu2YPgoApH1viOpZkL4/QqO28QeAcFPvxzZMmIpzhljwJQ9LHvmJS3v7bRmkzJfY9r98rArlxVRZEMA2TJwDizp6N6FtYbtrbN04SSUCeP0j4D4ZmwLGLr7Wh6JSc/uqH7d58lsQESwpXadmYScoXTedceEtpZGyuPNP3OGvn5fyLMBvMIlN8LQP0vjrP1jatLdwIi6TRsbDULQ37FD+hZx3SrZ+XsiFt5JGyrKehdzOmcMArrh8FriXJS/UzueNPjWUZX4xEZZ2L5WiVBbWAi6lfanWXDg5tKioyE97OnNiWeq7VyHEzz0hoX40Uk5x6bOGu3sm4JMj8h3ayKPP60Mnignb8/7TsLC9pAmchQbA5U0f3tBqdXVyZfPzzr9duvG9GkmkEGL6lnLn4h5192xAe+/3vC7yqn7rO000ALldnN7etGKwWooSTQva4cj4olCde3q0UFtqtXrMlfUzy7iwIEmkVKeM2+nu+ay1iFHWe6IafTFnefmVgOI981NNkR3dmKlAKN34QbEm9/T40tJS0fY0pw7MuJY08aa7kXI3qjcrOJIoyW0F2pwKUR1BdJfbP7ynNfCxzXOIxyFcbgsKiF6v727IiD1bE9lZ1EyVrXunUp17ZmxhYaHLtoxGo7/6zJGPrye8aLbMFwLtVS3uwQyZcTsNBuNDUp8RR4qsDTCgVKBQS4IcbRXbvDXyzmYgWsppSxHRarU9i9IjMhxJIfNzZf2Mm9pT+6ddunRJkrnAiT5Qffrg51fXTKqCUP867d1ZNoAZDiZs06rzfJaJDnxG5CLgk+ccXwhaBrIcWw6RvnoCGWI2bOlg2vKS4B643mDoXpgefpa8KFsHylKn/6jJPz9Z6Poq3doA84nvh4NOeCrAkfLpjVUv1MY0NZEdQHs0NQ0JE1x7Mh2Z3d2cE9re077hKKKEiJcFPDMhkIMwR1GPzZyf1IPF9tuNscZBlvKi4FFGBmPBYxe3f4MTc0uoWPMqU+ed+53QdTUXNwVwySNjILKNybx18iyhay5evEjma25l7FAwR7QFY0b0CTR5ggpgK57oAxEti1hMn901tytkF9agYruB9AQ7e5yzzDHz6tlZ4PZ++CjE9jtea0IWtV/Pkkd3FLpWk3tmpDFjWYb2xK5PcnNznf5ec3E7kjHqnxAeZLa0tbBtpXnj+GlCbSEBAbqs9dHGfUsOaTVqwWNdIX5wT4gIPlU7Z8UNiuOOh0g6+8pqnqjkoMCF0mmUml38nUwbJVT0qxczxmWHtsZOptQmJfBgsLjTGi5xuNMbW1ZWRvNAu+LiYqcNJpPhB3/zpglv0SpunYk/6uFy8443X4HLaU7fbywoeKigoKCrELlc8pjO2FbdA2jCAqtZ8vPfc5cOiKaAWpK0Qy1pp9tcKJueMQvxCfBZjTvAdVkd5Qi/SKZPvpYlCpeDwcOKJxIcJ9daUiLbprKkEZLexuq8mBbchnGfoQJ/EuoQi2xzx7z5v6dVlaRKGv5s9TA0U8GZgmYmLLCGrXp2pVm3wel4DOAPy/wQXNeX0DkqryJpbezuozlmMrg+SpB2LSMhRJ5XJ0ng0N9as/ghSyG8hYv9BT8TjpQIyEtwa7e5DeP/yBa2EySjlpQlnS+Z06a4XUBku/7QBueyNHB1okNYoIkl/nwu06fVeTb821jgXVixUUF5W/2Fgkh8+ymdiJL0UlyMFlq1GCVP2xKESxnzvcjIcAIXP8hlxoY5+7thOFdIWgVm/360/G7poU6u2mNRXaKktEVJE+Ytk+qcWYKfLxO5npbkqdbE7ctF5Ql43e8QxSJteT+DpfjIyr9ULn/O5I6UyuXPmgpO737fVVsGXV6fiuQ3blCQ6Kotc/hDULpttrq8vNSlUgoPx0fejXrcLSE3Vo+7XZCzY6z9vcDvvTtem4Vvv+xDMNGkUUL3Kaf2QlV/ltuWW9Hp9R10WRuSKpc/Lfpm313ahzMcWplkLCx0Gb2Wl5ertCfTP7uW+MptFiqcfcKQ+PK175RpzmVPcPdser2+a2F62MmaRY+ImVK4FTOU0x3fGlFYWFRnchcghMzeTE/1hPf+DzjOY74ghIQ8HN2xzauqFvdw6nTNws6gP5y4XafTSXqzUDGBmrPHZl1NmuS0MmxZXkmeWqW5kPO61Ihek587AGOTc9WLuzqRcTPuF5w2JyMO3WYnT0uAEHrhBBc8pQjwNYiV9UIIicFobFdwIDqtaklPu5HRG4yZKzK0Wp3TNihc36uqUq95hF1Y7eT+UVyhPZXxwY1VL5rqkLHu9zc050++je6y08aR6cLK1qbzMd0cPyfRqi/0KdwXeZRWku+Z0GfM+mMbwrEtwQPIRAgZ4YlurO2NhHtFRDZ8JHJtD+BLIKhK6+9InMu5UlQ0+ef6FKWHnKyKeswyMorSww4gGYL7EeY9M4exFf+VweKenC6UmIAReJD+6LpFt6KHWob59YRxd3Qn9syqqKhwIgNy56kgutd3bHn//aZDf+3h1Bg9W965ISXbZhfRVnD14m5gPLgiBUetaMK0jwmhkbIU0cvhGirtno44amfeKP5Jt9w/z4MvxpHSRZeVuk1/KCFLbzAIRuk1OWF92dKuvH8fGoBu5/BJQtehWWqhydkfVbz1S5M698x7OMc4mama2+V+LLrX321L8SzuibPVl/cKrvBqNOpBhv1LSnX/WZ+OQaTLmkAfEkLKHoCo+/dQVS/87CCIu+gUVmCsJ397gExOO6OxQDBbw7z3vf4sptfZOl8WFliCI2USd/hrJ68JSWlpNBqfFSID4LKKxfb/BMIC6mSvsJWDt5izvnI67JhGIhLRG+F2cdEHhBAJFGjeKx5NtXzeHfEVSD91uxDxAdAezDxPn8Yq5qNfdWPxg/YI7mFEtCxnK596BeCapLY4bYo/W9b9NQgPci7aDG/BcYnPJZkz/+LxCdReJ2QeD7v2qRr4Z8BnUcpdrKRg89+IZzxOxEAyerOY3ufFNpR4RQZdY7F9x8CPP7psizu72p/FDvgYzZ34mhFVXcUN3G06v8ijpW8RQka6v1NS23QcB5VrC+2l2ECnRajB9boY/aDZQjRjglODqNzRxAVzaEZcklE7UoLz2Nqxw8kciQlbMXACkueuAIdMITMnj5jvodIcCaG3+FVP2rJrk+oWZ0LdsmpHUMEQrQoPRvRGjAd+8VLsetukP1pyLkBJSUlw+YY/OEeqoqS0Kmcpvx4m1BaSNQjNm6Tjl8ijKtk9N8FD5QlF6rRiLHtPA2JrJ/V9LhRLOI54itbCHJ6Fjp2aC66PLiTPTVKCoEXU6rzhJVs/KzUvaCuNlPCgErZyyDNQVWa5n2WH+7O4wVPxc0mpRKbI9nBx59yTOr1eMDZxq0TeRju2S8pciRgIEn/fEK/rhVgC4qaHRh6dz/IxFRWJtsOT2g+xAsTL7rbK6qQ6P/fl0s0fldBOoSRSIttms+QX+kH1VRWLHzISR84laWR0gJJtX6gxove4FhB40yL0RhIptH1L8YLoqdbAL99PAN7NFRsVdJop/VrcIKkjD0mzmT2hbYETsjuqOZc9tnzdu9ckzSeERR2PspRfTUAyxFZM64CFBeHImJOnUecOdJe94rLj8y0ZjdEg7gHRJJ8A5LaGOZkYWkxcDuIlD0SQFvGmJyVyVneZzgJz3DSTTwjGFH6a04enXE2ecodJLV8LD5KUJU+JE6WbZhVr8s565XRQbLM98DGCmIkgxZIn9IX19606IKYBvzklNiooOMRAVtUNwj3fYwd+wndMtJBPCAkGZgG67LRvKpJfuyM5LdQNLAkTKa/d0OXsE4z6Pe44f7gmpZoedjFaKO2Hattpr0RsjqN7aft2oje2b62j0LGI1TNCSNCc+GvOZ0++umaSF2pE/KBk6+zL6vy8CVILduSK9Vgn+mVpuWdtgfWe18CLRzh5nRASWkLXnDny0Y2EX1dJnlMEzFRFypsV6rzzz/uKDHsB3tOhucV9HMS7ohQA9q/TBp9LTJ6ax4GmTwghoaV0fVZqlGXXUbb58oPrq39TqT2Z7nIn0tsCfCLDFKuJEjJj9BnNI9PR5LVyuDcY+FRTKnnwKGi1tuMbQkh0On2w9uTur68njpdRiesH5eveqdacyphhxDnJKw8iU4Avi6MJusDu2cgB+Ac4lMIBv3Y1Avg8YJt3FCLWtoTv9h0hJAaDoZUue1vIrZgh0kZG4niT5vTBP1GOr9cewgOxjhbKfKciUtpU+hUInKEF/HmPxxz60nAJsYk+a33K3aheLgm5GfdLJOPQbK9/uQ8Fn7sv8GtY9n0Ju4/2ugoQ7H1C0CVuozmxJ/lW7FBBMu4s6w+anIzQAoXMlKciQsiu+2jvaXB2LLxPCAkGj61xol91d2lvu+CKkhJ+WYNkRSMZD9yxeiKEkMs/Qc4vKlij9LbAn6rt+ML6hhASjFMeMmYu30X73/Rlt2KGmnXHtz5wI8MmwEfWWgEl0gbbApBQuWVNvBtkdQyEVgKyfdoJrfpCz4KMpZnXV49jhiNJMTqd7oE9b8TFWw1W5ZKb/AY5CSL307GD/wLXW72LfdqJK1euqDTqvCe1Ofv/odVq5e2KNTCxHktOh2q6KgunHUCqyhpQe988CxlUu0gnoLoqd6B1rebfwZIrwBeX7nTlRQK/Hka5xXQK3g/g+qAcWnX+ukmcVuQrAX4HkA7bzBaZC6SAHIIDiDH1XpnVGIWqqIDfTaQR4LL8QgBk9ujk7i7kdTWLFwX4bMUXgI+63Y0Ws9XDGgzNP2XpO7FO3J2AXwMTW96nxcipYJdo1yz1IKjwJxEb7EYLrRzH4qQt6eDm/weokFF19JLhQAAAAABJRU5ErkJggg=="
              />
            </defs>
            <style>
              tspan {
                white-space: pre;
              }
            </style>
            <use id="Background" href="#img1" x="0" y="0" />
          </svg>
        </div>
        <p></p>
      </a>
      <a href="https://sol.apefinance.org/" target="_blank" class="card education">
        <div class="overlay"></div>
        <div class="circle">
          <svg
            version="1.2"
            baseProfile="tiny-ps"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 100 100"
            width="100"
            height="100"
          >
            <title>Background</title>
            <defs>
              <image
                id="img2"
                width="100"
                height="100"
                href="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGQAAABkCAMAAABHPGVmAAAAAXNSR0IB2cksfwAAAPxQTFRFAAAA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gA/4gApZ+XcgAAAFR0Uk5TAAVr4f/HdQqjqA/RhCb3QujwSswfjMRulJl7Ltm6oVdmOJxIeDMrEhoUAxeu3ubW2+BM463C9UWrv3CP+paKYesI/Ie4gFyekSS9aablhfIhR3opwvzPSQAAAp5JREFUeJztmmt70jAUx9N6aFknbB2ogBfKlNmJK8PBVOi2qnMX1Hn7/t/FpEkvCZXVxyYv9uT/pkl6kl+bnJLTUxDiZZj3oGrVRIZVOQKLZ9h1GYwNjuFsymDc5xgNGYymxTG2tiUw3B3VDDlu1WpzjAcyGA8dBa7LMbTrrpF610WPJCAE10XIlcDgXVfKnbgdkaGlpVVCjW7V6j1egTyp/IkH1xIhT6uHiPuVmp1XTZyiiqJkc1RFURGwYCeT4srPtCv/J0W78m1qChA5rixCkN33qtZgBaKlpXW7BtX/sOwKCBXpQUl5HI6hYgtWEbLclTzOcwkIcLn3IRWRigq30q5bnnFHXBchGfexEmS/qBxRkB60h1VrzxAZWlpaWlpaWqJe+kz7Qt2nm7Xt77/iOhipwchgdTs7RXff1CSut18fBEzj+LSV1oPDHuncCyZ7ecabWmpwNCWBiRUEG4yCi318cKapSTAbonYWEx2/JWZ8IEZ6dAGG+Rs/yBt0qAHUKQUXPXyY5k220TuA9+zrCo3IPIBDK85TzccA3VXIEEc9ZhyXDBY4xmKQ8MTJQVoApzR2OTvGb79NiD5wE44hJiuaf4O0+CI2COHjJ4ODJIERLqJNCE0WMKUQL+OVhZyeQ/MzB0nMSbHfTOcuuigLidgET1OI51xCeGXkIMknrojwrKNs5RslITklEHS9BPeLkUFywg0jNlt4Fb+WhHwzaQrzJgdB/jl8NzPInKU5Iy7t4dMeeOT5v68JGXm0jK+7YE0Q2mGTV8PLR0eO6rRlkj4GXhJN/1gDITNWDLFvspUfE1f/WfQwpjpZByEzVgjZypzrMp4Uo5P9bSJaEOwit8wjfL0uLNkA1xOY4cMvCC9ow+8ZACnOwE0guOUPBRKuVUsVtBwAAAAASUVORK5CYII="
              />
            </defs>
            <style>
              tspan {
                white-space: pre;
              }
            </style>
            <use id="Background" href="#img2" x="0" y="0" />
          </svg>
        </div>
        <p></p>
      </a>
    </div>
  </div>
</template>

<script lang="ts">
import { Vue, Component } from 'nuxt-property-decorator'

import { Button } from 'ant-design-vue'

@Component({
  layout: 'single',

  components: {
    Button
  }
})
export default class Index extends Vue {}
</script>

<style lang="less" scoped>
@media only screen and (min-width: 700px) {
  .container {
    max-width: 450px;

    .change-side {
      div {
        height: 32px;
        width: 32px;
        border-radius: 50%;
        background: #000829;
        cursor: pointer;
      }
    }
  }
  .big_div {
    width: 100%;
  }
  .node_div {
    width: 80%;
    margin: 0 auto;
  }
  .font_color_1 {
    color: rgba(241, 241, 242, 1);
  }
  .font_color_2 {
    color: #84879c;
  }
  .font_center {
    text-align: center;
  }
  .image_div {
    position: relative;
    .image {
      position: absolute;
      width: 932px;
      height: 780.35px;
      right: 0;
    }
    .image2 {
      position: absolute;
      right: 0;
      top: -50px;
    }
    .image3 {
      position: absolute;
      top: -50%;
      width: 450px;
      height: 500px;
    }
    .image4 {
      position: absolute;
      right: 0;
      top: -50%;
    }
  }
  .image5 {
    width: 70%;
  }
  .title {
    font-weight: 100;
    letter-spacing: -0.02em;
    color: #f1f1f2;
    font-size: 88px;
    line-height: 1.1;
  }
  .defiText {
    font-weight: 600;
    background: -webkit-linear-gradient(90deg, #fff 0%, #c19159 50%, #f80 100%);
    background-clip: text;
    -webkit-text-fill-color: transparent;
  }
  .subtitle {
    font-weight: 300;
    letter-spacing: -0.02em;
    color: #f1f1f2;
    opacity: 0.5;
    font-size: 32px;
    padding-top: 40px;
  }
  .button_div {
    width: 220px;
    height: 60px;
    .button_font {
      text-transform: uppercase;
      color: #fff;
      margin-top: 15px;
      text-align: center;
      font-weight: bold;
      font-size: 20px;
    }
  }
  .button_div_line {
    border: 1px solid #fff;
    border-radius: 5px;
    margin-left: 40px;
    left: 220px;
  }
  .title_line {
    font-size: 40px;
    .weight_title {
      font-weight: bold;
    }
  }
  .node_p {
    font-size: 20px;
  }
  .solana_log {
    float: right;
    padding-top: 166px;
  }
  .float_left {
    float: left;
  }
  .float_right {
    float: right;
  }
  .ecosystemwide {
    padding-top: 40px;
  }
  .node_width {
    width: 450px;
  }
  .logo {
    padding-bottom: 170px;
    padding-top: 100px;
  }
}
@media screen and (max-width: 700px) {
  .hidden {
    word-break: keep-all;
    overflow: hidden;
    text-overflow: ellipsis;
  }
  .container {
    max-width: 450px;

    .change-side {
      div {
        height: 32px;
        width: 32px;
        border-radius: 50%;
        background: #000829;
        cursor: pointer;
      }
    }
  }
  .big_div {
    width: 100%;
  }
  .node_div {
    width: 70%;
    margin: 0 auto;
  }
  .font_color_1 {
    color: rgba(241, 241, 242, 1);
  }
  .font_color_2 {
    color: #84879c;
  }
  .font_center {
    text-align: center;
  }
  .image_div {
    position: relative;
    .image {
      position: absolute;
      // width: 932px;
      // height: 780.35px;
      right: 0;
      width: 100%;
    }
    .image2 {
      position: absolute;
      right: -90%;
      top: -40px;
      z-index: 0;
    }
    .image3 {
      position: absolute;
      top: -30%;
      width: 450px;
      height: 500px;
      left: -80%;
    }
    .image4 {
      position: absolute;
      right: -60%;
      top: 0;
    }
  }
  .title {
    font-weight: 100;
    letter-spacing: -0.02em;
    color: #f1f1f2;
    font-size: 9vw;
    line-height: 1.1;
  }
  .defiText {
    font-weight: 600;
    background: -webkit-linear-gradient(90deg, #5ac4be 0%, #3772ff 50%, #c200fb 100%);
    background-clip: text;
    -webkit-text-fill-color: transparent;
  }
  .subtitle {
    font-weight: 300;
    letter-spacing: -0.02em;
    color: #f1f1f2;
    opacity: 0.5;
    font-size: 32px;
    padding-top: 20px;
    width: 100%;
  }
  .button_div {
    width: 40%;
    min-width: 130px;
    height: 50px;
    .button_font {
      text-transform: uppercase;
      color: #fff;
      margin-top: 15px;
      text-align: center;
      font-weight: bold;
      font-size: 15px;
    }
  }
  .button_div_line {
    border: 1px solid #fff;
    border-radius: 5px;
    margin-left: 40px;
    left: 40%;
  }
  .title_line {
    font-size: 40px;
    .weight_title {
      font-weight: bold;
    }
  }
  .node_p {
    font-size: 20px;
  }
  .solana_log {
    float: right;
    padding-top: 66px;
  }
  .float_left {
    float: left;
  }
  .float_right {
    float: right;
  }
  .ecosystemwide {
    padding-top: 40px;
  }
  .text_align_right {
    text-align: right;
  }
  .logo {
    padding-top: 50px;
    padding-bottom: 50px;
  }
  .image5 {
    width: 100%;
  }
  #animation_container {
    flex-direction: column;
    align-items: center;
  }
}
.education {
  --bg-color: #ffd861;
  --bg-color-light: #ffeeba;
  --text-color-hover: #4c5656;
  --box-shadow-color: rgba(255, 215, 97, 0.48);
}

.credentialing {
  --bg-color: #b8f9d3;
  --bg-color-light: #e2fced;
  --text-color-hover: #4c5656;
  --box-shadow-color: rgba(184, 249, 211, 0.48);
}

.wallet {
  --bg-color: #ceb2fc;
  --bg-color-light: #f0e7ff;
  --text-color-hover: #fff;
  --box-shadow-color: rgba(206, 178, 252, 0.48);
}

.human-resources {
  --bg-color: #dce9ff;
  --bg-color-light: #f1f7ff;
  --text-color-hover: #4c5656;
  --box-shadow-color: rgba(220, 233, 255, 0.48);
}

.card {
  width: 320px;
  height: 400px;
  background: #fff;
  border-radius: 10px;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  position: relative;
  margin: 20px 30px;
  box-shadow: 0 14px 26px rgba(0, 0, 0, 0.04);
  transition: all 0.3s ease-out;
  text-decoration: none;
}

.card:hover {
  transform: translateY(-5px) scale(1.005) translateZ(0);
  box-shadow: 0 24px 36px rgba(0, 0, 0, 0.11), 0 24px 46px var(--box-shadow-color);
}

.overlay {
  width: 118px;
  position: absolute;
  height: 118px;
  border-radius: 50%;
  background: var(--bg-color);
  top: 119px;
  left: 102px;
  z-index: 0;
  transition: transform 0.3s ease-out;
}

.card:hover .overlay {
  transform: scale(6) translateZ(0);
}

.circle {
  width: 180px;
  height: 180px;
  border-radius: 50%;
  background: #fff;
  border: 2px solid var(--bg-color);
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  z-index: 1;
  transition: all 0.3s ease-out;
}

.circle::after {
  content: '';
  width: 162px;
  height: 162px;
  display: block;
  position: absolute;
  background: var(--bg-color);
  border-radius: 50%;
  top: 7px;
  left: 7px;
  transition: opacity 0.3s ease-out;
}

.card:hover .circle::after {
  background: var(--bg-color-light);
}

.card:hover .circle {
  border-color: var(--bg-color-light);
  background: var(--bg-color);
}

.card p {
  font-size: 17px;
  color: #4c5656;
  margin-top: 30px;
  z-index: 1000;
  transition: color 0.3s ease-out;
}

.card:hover p {
  color: var(--text-color-hover);
}

.card:active {
  transform: scale(1) translateZ(0);
  box-shadow: 0 15px 24px rgba(0, 0, 0, 0.11), 0 15px 24px var(--box-shadow-color);
}

.circle svg {
  z-index: 10000;
  transform: translateZ(0);
}
</style>
