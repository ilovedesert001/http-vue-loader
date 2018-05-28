
<tags>

    <tag name="hello1">
        <template>
            <div>
                <tag1></tag1>
                <br>
                id:{{ _uid }}
                <br>
                hello {{ msg }} : {{ time }}

                <button @click="btn1">这是个按钮</button>
            </div>
        </template>

        <script>
            module.exports = {
                data() {
                        return {
                            msg: 'Vue',
                            time: 0
                        }
                    },
                methods: {
                    btn1:function () {
                        this.time = 0;
                    }
                },
                    created: function () {
                        var vm  =this;
                        setInterval(function () {
                            vm.time += vm._uid;
                        }, 1000);
                    },
                }
        </script>

    </tag>

    <tag name="hello2">
        <template>
            <h1>
                id:{{ _uid }}
                hello {{ msg }} : {{ time }}
            </h1>
        </template>

        <script>

            module.exports = {
                data() {
                    return {
                        msg: 'Vue',
                        time: 0
                    }
                },
                created: function () {
                    var vm  =this;
                    setInterval(function () {
                        vm.time += vm._uid;
                    }, 1000);
                },
            }
        </script>

    </tag>

</tags>