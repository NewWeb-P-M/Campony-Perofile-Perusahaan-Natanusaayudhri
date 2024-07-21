<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div class="maintextview1"
        data-aos="fade-right"
       data-aos-duration="1000"
        data-aos-easing="ease-in-sine"
    >
        <div class="isitext">
            <div class="text1">
                <p>Konsultan SLF terpercaya</p>
            </div>
            <div class="text2">
                <p>Mencari jasa pengkaji teknis dan konsultan SLF profesional?</p>
            </div>
            <div class="text3">
                <p>PT Spektra Wahana Bahtera adalah solusi yang tepat untuk menjadi mitra dalam mengurus segala ijin
                    bangunan gedung, baik PBG, SLF, ijin lingkungan, rekomendasi K3, dan lainnya</p>
            </div>
        </div>
    </div>
</template>

<style>
.text3 p {
    font-size: 15px;
}
.text1 p{
    font-size: 22px;
    font-weight: bold;
    color: #3687aa;
}
.text2{
    font-weight: bold;
    font-size: 30px;
}
.maintextview1 {
    text-align: left;
    display: flex;
    height: 500px;
    justify-content: left;
    align-items: center;
}
.isitext{
    /* position: absolute; */
    width: 500px;
    margin-left: 50px;
}
p{
    color: black;
}

@media (max-width: 600px) {
    .maintextview1{
        text-align: left;
        display: flex;
        height: 500px;
        justify-content: left;
        
    }
    .isitext{
        margin-left: 10px;
    }
    .text2{
        font-size: 20px;
    }
    .text1 p{
        font-size: 15px;
    }
    .text3 p{
        font-size: 12px;
    }
}

</style>
