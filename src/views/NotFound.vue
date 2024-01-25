<template>
    <div>
        <div class="errcover">
            <div class="errCenter">
                <div class="errLeft">
                    <div class="errDigits">404</div>
                    <div class="errText">We are sorry, but the page you requested was not found</div>
                    <router-link to="/">
                        <div class="top__button">
                            <div class="top__button-text">Back To Home</div>
                            <svg class="top__button-img" xmlns="http://www.w3.org/2000/svg" width="18" height="17"
                                viewBox="0 0 18 17" fill="none">
                                <path d="M1 8.43542L14.7232 8.29857M9.61818 1.91138L16.1412 8.43436L9.48677 15.0887"
                                    stroke="#CDA274" stroke-width="2" stroke-linecap="square" stroke-linejoin="round" />
                            </svg>
                        </div>
                    </router-link>
                </div>
                <div class="errImg"><img src="@/assets/err.png" alt=""></div>
            </div>
        </div>


    </div>
</template>

<script>
export default {
    name: 'NotFound'
}
</script>

<style lang="scss" scoped>
// div {
//     background-image: url("@/assets/404_fullhd_rus.webp");
//     height: 1000px;

// }
.errCenter {
    display: flex;
    // justify-content: center;

    width: 1563px;
    // gap: 81px;
}

.errcover {
    display: flex;
    justify-content: center;
}

.errLeft {
    display: flex;
    width: 569px;
    flex-direction: column;
    gap: 23px;
    flex-shrink: 0;
    justify-content: center;
}

.errDigits {
    color: #CDA274;
    font-family: "DM Serif Display";
    font-size: 250px;
    font-style: normal;
    font-weight: 400;
    line-height: 125%;
    text-align: left;
    /* 312.5px */
}

.errText {
    color: #292F36;
    font-family: "DM Serif Display";
    font-size: 35px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    /* 52.5px */
    letter-spacing: 0.35px;
    text-align: left;
}

.errLeft .top__button {
    width: 253px;
}
</style>