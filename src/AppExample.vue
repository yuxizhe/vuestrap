<template>
    <!-- 内容 -->
    <accordion type="info">
        <panel is-open type="primary">
            <strong slot="header"><u>Panel #1</u></strong> ...
        </panel>
        <panel header="Panel #2">
            ...
        </panel>
        <panel header="Panel #3">
            ...
        </panel>
        <panel header="Panel #4">
            ...
        </panel>
    </accordion>
    <!-- 目录 -->
    <affix offset="50">
        <ul>
            <li>...</li>
            <li>...</li>
            <li>...</li>
        </ul>
        <a href="#">...</a>
    </affix>
    <!-- 侧栏 -->
    <button class="btn btn-success btn-lg" @click="sideopen=!sideopen">侧栏</button>
    <aside :show.sync="sideopen" placement="left" header="侧栏" width="350">
        侧栏
    </aside>
    <!-- 幻灯片 -->
    <carousel interval="5000">
        <slider>
            <img src="https://placehold.it/1200x400?text=one">
            <div class="carousel-caption">
                ...
            </div>
        </slider>
        <slider>
            <img src="https://placehold.it/1200x400?text=two">
        </slider>
        <slider>
            <img src="https://placehold.it/1200x400?text=three">
        </slider>
    </carousel>
    <!-- 日期选择 -->
    <datepicker :value.sync="time" :disabled-days-of-week="disabled" :format="format" :clear-button="clear" :placeholder="placeholder">
    </datepicker>
    <!-- dropdown   测试不能用啊-->
    <dropdown>
        <button class="btn btn-default">
            Action
            <!-- <span class="caret"></span> -->
        </button>
        <ul slot="dropdown-menu" class="dropdown-menu">
            <li><a href="#dropdown">Action</a></li>
            <li><a href="#dropdown">Another action</a></li>
            <li><a href="#dropdown">Something else here</a></li>
            <li role="separator" class="divider"></li>
            <li><a href="#dropdown">Separated link</a></li>
        </ul>
    </dropdown>
    <br>
    <!-- modal  弹出框 -->
    <button class="btn btn-success btn-lg" @click="showmodal=!showmodal">modal</button>
    <modal :show.sync="showmodal">
        <div slot="modal-header" class="modal-header">
            <h4 class="modal-title">Modal title</h4>
        </div>
        <div slot="modal-body" class="modal-body">...</div>
    </modal>
    <!-- 标题栏 -->
    <navbar placement="top" type="default">
        <!-- Brand as slot -->
        <a slot="brand" href="/" title="Home" class="navbar-brand">VueStrap</a>
        <!-- You can use dropdown component -->
        <dropdown text="Dropdown">
            <li><a href="link">Option</a></li>
        </dropdown>
        <!-- Or normal bootstrap style -->
        <li class="dropdown">
            <a href="#" class="dropdown-toggle">Dropdown</a>
            <ul class="dropdown-menu">
                <li><a href="link">Option</a></li>
            </ul>
        </li>
        <!-- For right positioning use slot -->
        <li slot="right">
            <a href="https://github.com/yuche/vue-strap" target="_blank">Fork...</a>
        </li>
    </navbar>
    <!-- popover -->
    <br>
    <popover effect="fade" placement="bottom" title="Title" content="content">
        <button class="btn btn-default">Popover on bottom</button>
    </popover>
    <br>
    <!-- 进度bar -->
    <div class="progress">
        <progressbar now="50" label="true" type="warning" striped></progressbar>
    </div>
    <div class="progress">
        <progressbar now="30" label type="primary" striped animated></progressbar>
    </div>
</template>
<script>
import {
    accordion,
    affix,
    panel,
    aside,
    carousel,
    slider,
    datepicker,
    dropdown,
    modal,
    navbar,
    popover,
    progressbar
} from 'vue-strap'

export default {
    data() {
            return {
                sideopen: false,
                time: '',
                showmodal: false
            }
        },
        components: {
            accordion,
            affix,
            panel,
            aside,
            carousel,
            slider,
            datepicker,
            dropdown,
            modal,
            navbar,
            popover,
            progressbar
        }
}
</script>
