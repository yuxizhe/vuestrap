<template>
    <div class="container">
        <div class="row clearfix">
            <div class="col-md-12 column">
                <nav class="navbar navbar-default navbar-fixed-top" role="navigation">
                    <div class="navbar-header">
                        <button type="button" class="navbar-toggle" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1"> <span class="sr-only">Toggle navigation</span><span class="icon-bar"></span><span class="icon-bar"></span><span class="icon-bar"></span></button> <a class="navbar-brand" href="#">明其道不计其功</a>
                    </div>
                    <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
                        <ul class="nav navbar-nav">
                            <li>
                                <a v-link="{path: '/3'}">聊天室</a>
                            </li>
                            <li>
                                <a v-link="{path: '/movie'}">电影</a>
                            </li>
                            <li>
                                <a v-link="{path: '/smzdm'}">值得买</a>
                            </li>
                            <li>
                                <a v-link="{path: '/2'}">菜谱</a>
                            </li>
                            <li>
                                <a v-link="{path: '/blog'}">博客</a>
                            </li>
                        </ul>
                        <ul class="nav navbar-nav navbar-right ">
                            <li class="dropdown ">
                                <a href="# " class="dropdown-toggle " data-toggle="dropdown ">Dropdown<strong class="caret "></strong></a>
                                <ul class="dropdown-menu ">
                                    <li>
                                        <a href="# ">Action</a>
                                    </li>
                                    <li>
                                        <a href="# ">Another action</a>
                                    </li>
                                    <li>
                                        <a href="# ">Something else here</a>
                                    </li>
                                    <li class="divider ">
                                    </li>
                                    <li>
                                        <a href="# ">Separated link</a>
                                    </li>
                                </ul>
                            </li>
                        </ul>
                    </div>
                </nav>
            </div>
        </div>
    </div>
    <div class="routerview">
        <router-view></router-view>
</template>
<style type="text/css">
.routerview {
    margin-top: 60px;
}
</style>
