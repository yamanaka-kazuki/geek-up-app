<template>
    <div class="sidebar-page">
        <section class="sidebar-layout">
            <b-sidebar
                position="static"
                :mobile="mobile"
                :expand-on-hover="expandOnHover"
                :reduce="reduce"
                :delay="expandWithDelay ? 500 : null"
                type="is-light"
                fullheight
                open
            >
                <div class="p-1">
                    <b-menu class="is-custom-mobile">
                        <b-menu-list label="">
                            <b-menu-item
                                icon="database-outline"
                                label="ダッシュボード"
                                class="mb-24"
                            ></b-menu-item>
                            <b-menu-item
                                icon="folder-pound"
                                label="学習リスト"
                                class="mb-24"
                            >
                            </b-menu-item>
                            <b-menu-item
                                label="プロフィール"
                                icon="account"
                                class="mb-24"
                            ></b-menu-item>
                            <b-menu-item label="設定" icon="cog"></b-menu-item>
                        </b-menu-list>
                    </b-menu>
                </div>
            </b-sidebar>
        </section>
    </div>
</template>

<script>
export default {
    data() {
        return {
            expandOnHover: true,
            expandWithDelay: true,
            mobile: 'reduce',
            reduce: false,
        };
    },
};
</script>

<style lang="scss">
.p-1 {
    padding: 3em;
    margin: 30px 0;
}

.mb-24 {
    margin-bottom: 24px;
}

.sidebar-page {
    display: flex;
    flex-direction: column;
    width: 100%;
    // min-height: 100%;
    min-height: 100vh;
    .sidebar-layout {
        display: flex;
        flex-direction: row;
        // min-height: 100%;
        min-height: 100vh;
    }
}
@media screen and (max-width: 1023px) {
    .b-sidebar {
        .sidebar-content {
            &.is-mini-mobile {
                &:not(.is-mini-expand),
                &.is-mini-expand:not(:hover):not(.is-mini-delayed) {
                    .menu-list {
                        li {
                            a {
                                span:nth-child(2) {
                                    display: none;
                                }
                            }
                            ul {
                                padding-left: 0;
                                li {
                                    a {
                                        display: inline-block;
                                    }
                                }
                            }
                        }
                    }
                    .menu-label:not(:last-child) {
                        margin-bottom: 0;
                    }
                }
            }
        }
    }
}
@media screen and (min-width: 1024px) {
    .b-sidebar {
        .sidebar-content {
            &.is-mini {
                &:not(.is-mini-expand),
                &.is-mini-expand:not(:hover):not(.is-mini-delayed) {
                    .menu-list {
                        li {
                            a {
                                span:nth-child(2) {
                                    display: none;
                                }
                            }
                            ul {
                                padding-left: 0;
                                li {
                                    a {
                                        display: inline-block;
                                    }
                                }
                            }
                        }
                    }
                    .menu-label:not(:last-child) {
                        margin-bottom: 0;
                    }
                }
            }
        }
    }
}
.is-mini-expand {
    .menu-list a {
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;
    }
}
</style>
