<template>
    <div>
        <div class="left-navbar">
            <div class="nav-logo">
                <h2 class="logo-title">Taxi</h2>
            </div>

            <div class="nav-menu">
                
                <el-menu default-active="2" class="el-menu-vertical-demo" >
                    <el-menu-item index="1">
                        <nuxt-link exact :to="{ name: 'dashboard' }">
                            <span class="icon-menu">
                                <i class="el-icon-s-home"></i>
                            </span>
                            <span>Dashboard</span>
                        </nuxt-link>
                    </el-menu-item>
                    <el-menu-item index="2">
                        <nuxt-link exact :to="{ name: 'dashboard-orders' }">
                            <span class="icon-menu">
                                <i class="el-icon-user-solid"></i>
                            </span>
                            <span>Buyurtmalar</span>
                        </nuxt-link>
                    </el-menu-item>
                    <el-menu-item index="2">
                        <nuxt-link exact :to="{ name: 'admin-pupils' }">
                            <span class="icon-menu">
                                <i class="el-icon-box"></i>
                            </span>
                            <span>Marshrut</span>
                        </nuxt-link>
                    </el-menu-item>

                    <el-submenu index="3">
                        <template slot="title">
                            <span class="icon-menu">
                                <i class="el-icon-user-solid"></i>
                            </span>
                            <span>Foydalanuvchilar</span>
                        </template>
                        <el-menu-item-group>
                            <el-menu-item index="1-1">
                                <nuxt-link
                                    nuxt-link-exact-link
                                    :to="{ name: 'admin-regions' }"
                                >
                                    Foydalanuvchilar
                                </nuxt-link>
                            </el-menu-item>

                            <el-menu-item index="1-3">
                                <nuxt-link
                                    nuxt-link-exact-link
                                    :to="{ name: 'users-client' }"
                                >
                                    Haydovchilar
                                </nuxt-link>
                            </el-menu-item>
                            <el-menu-item index="1-3">
                                <nuxt-link
                                    nuxt-link-exact-link
                                    :to="{ name: 'users-client' }"
                                >
                                    Rahbariyat
                                </nuxt-link>
                            </el-menu-item>
                        </el-menu-item-group>
                    </el-submenu>

                    <el-menu-item index="4">
                        <nuxt-link exact :to="{ name: 'category' }">
                            <span class="icon-menu">
                                <i class="el-icon-files"></i>
                            </span>
                            <span>Kategoriya</span>
                        </nuxt-link>
                    </el-menu-item>
                    <el-menu-item index="4">
                        <nuxt-link exact :to="{ name: 'statistica' }">
                            <span class="icon-menu">
                                <i class="el-icon-s-help"></i>
                            </span>
                            <span>Statistika</span>
                        </nuxt-link>
                    </el-menu-item>

                    <el-menu-item index="5">
                        <nuxt-link exact :to="{ name: 'settings' }">
                            <span class="icon-menu">
                                <i class="el-icon-s-operation"></i>
                            </span>
                            <span>Settings</span>
                        </nuxt-link>
                    </el-menu-item>
                </el-menu>
            </div>
        </div>
        <header>
            <div class="header-inner">
                <div class="header-left">
                    <nuxt-link to="/moderator">
                        <i class="el-icon-back"></i>
                    </nuxt-link>
                </div>


                <div class="header-right" @click="logOut2">
                    <el-dropdown>
                        <span class="el-dropdown-link">
                             Xushnudbek 
                            <i class="el-icon-arrow-down el-icon--right"></i>
                        </span>
                        <el-dropdown-menu slot="dropdown">
                            <el-dropdown-item icon="el-icon-user"
                                >Profile</el-dropdown-item
                            >
                            <el-dropdown-item icon="el-icon-s-tools"
                                >Settings</el-dropdown-item
                            >

                            <el-dropdown-item
                                class="danger-text"
                                icon="el-icon-switch-button"
                                divided
                                >Log out</el-dropdown-item
                            >
                        </el-dropdown-menu>
                    </el-dropdown>
                </div>
            </div>
        </header>
    </div>
</template>

<script>
export default {
    data() {
        return {
            isCollapse: true,
        };
    },
    methods: {
         handleOpen(key, keyPath) {
            console.log(key, keyPath);
        },
        handleClose(key, keyPath) {
            console.log(key, keyPath);
        },
     
    },
};
</script>

<style lang="scss" scoped>
.header-left {
    a {
        font-size: 28px;
        color: #000;
    }
}
.el-menu-vertical-demo:not(.el-menu--collapse) {
    width: 200px;
    min-height: 400px;
}
</style>
