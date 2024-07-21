<template>
    <div class="destop">
        <div>
            <div class="navigasi">
                <ul>
                    <li><a href="https://mail.google.com/mail/u/0/#inbox?compose=new" class="titleCore"><i
                                class="bi bi-envelope-at"></i> hello@natanusaayudhri.com</a></li>
                    <li><a href="" class="titleCore"> <i class="bi bi-geo-alt-fill"></i> Grand Galaxy City, RSNB No. 22,
                            Bekasi</a></li>
                    <FeatherIcon icon="alert-circle" style="color: #000;" />

                </ul>
            </div>
            <div class="logoMain">
                <FeatherIcon icon="alert-circle" />
            </div>
        </div>
    </div>
</template>

<style scoped>
.navigasi {
    background-color: #3687aa;
    width: 100%;
    height: 50px;
    display: flex;
    list-style-type: none;
    justify-content: end;
    align-items: center;
    text-align: center;
}

.titleCore {
    color: white;
    text-decoration: none;
}

.navigasi ul {
    display: flex;
    list-style-type: none;
    justify-content: end;
    align-items: center;
    text-align: center;
}

.navigasi ul li {
    margin-right: 20px;
}
@media (max-width: 600px) {
  .destop {
    display: none;
  }
}
</style>
