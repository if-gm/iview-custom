<template>
    <div>
        <!--v.fixed = null,-->
        <!--columns3.map(v => (v.tooltip = true,v))-->
        <Table ref="currentRowTable"
               :columns="columns3.map(v => (v.tooltip = true,v))" :data="Array(2).fill(data1[0])" border
               @on-col-resize="saveColWidthToLocale"></Table>
        <Button @click="handleClearCurrentRow">Clear</Button>
    </div>
</template>
<script>
    export default {
        data() {
            return {
                columns3: [{
                    title: "客户名称",
                    fixed: "left",
                    width: 180,
                    key: "Z",
                }, {
                    title: "客户手机",
                    width: 150,
                    fixed: "left",
                    sortable: 'custom',
                    order: 'asc',
                    key: "AO",
                }, {
                    title: "所属公海",
                    key: "Z",
                    fixed: "left",
                    width: 120,
                    render(h, params) {
                    },
                }, {
                    title: "备注",
                    key: "V",
                    fixed: "right",

                    width: 120
                }, {
                    title: "最新跟进记录",
                    width: 150,
                    fixed: "right",

                    key: "E"
                }, {
                    title: "跟进状态",
                    width: 150,
                    fixed: "right",

                    key: "D"
                }, {
                    title: "创建时间",
                    key: "AA",
                    width: 150
                }, {
                    title: "电话",
                    key: "L",
                    width: 150
                }, {
                    title: "微信",
                    key: "N",
                    width: 150
                }, {
                    title: "QQ",
                    key: "O",
                    width: 150
                }, {
                    title: "邮箱",
                    key: "AL",
                    width: 150
                }, {
                    title: "客户类型",
                    key: "B",
                    width: 150
                }, {
                    title: "客户来源",
                    key: "S",
                    width: 150
                }, {
                    title: "客户需求",
                    key: "AH",
                    width: 150
                }, {
                    title: "合作培训经历",
                    key: "AG",
                    width: 120
                },],
                data1: [{
                    "id": "546981",
                    "lx": "1",
                    "A": "\u90ed\u5973\u58eb18317730854",
                    "B": "B(\u666e\u901a\u5ba2\u6237)",
                    "C": "",
                    "D": "12",
                    "E": null,
                    "F": null,
                    "G": null,
                    "H": "\u738b\u768e\u9759",
                    "I": "",
                    "J": "\u738b\u768e\u9759",
                    "K": "18317730854",
                    "L": "",
                    "M": "",
                    "N": "",
                    "O": "",
                    "P": "",
                    "Q": null,
                    "R": null,
                    "S": "\u767e\u5ea6\u7ade\u4ef7",
                    "T": "",
                    "U": "",
                    "V": "  \u5b66\u9020\u4ef7\u5b9e\u8bad\uff0c\u4e3a\u4e86\u8f6c\u884c\uff0c\u73b0\u5728\u662f\u4f1a\u8ba1\uff0c\u60f3\u8f9e\u804c\uff0c\u5173\u6ce8\u5c31\u4e1a",
                    "W": null,
                    "X": "\u5e02\u573a\u63a8\u5e7f\u90e8",
                    "Y": null,
                    "Z": "\u7ade\u4ef7\u4e13\u7528\u516c\u6d77",
                    "AA": "2019-01-18 19:58:54",
                    "AB": "2019-01-18 19:58:54",
                    "AC": null,
                    "AD": null,
                    "AE": "",
                    "AF": "",
                    "AG": "",
                    "AH": "",
                    "AI": "",
                    "AJ": "",
                    "AK": "3",
                    "AL": "",
                    "AM": "0",
                    "AN": "",
                    "AO": "",
                    "AQ": "",
                    "AR": "55",
                    "AT": "55",
                    "Bb": "27",
                    "Db": "\u521d\u8bbf",
                    "Zz": "3"
                }]
            }
        },
        methods: {
            saveColWidthToLocale(colmun) {
                console.log(colmun);
            },
            handleClearCurrentRow() {
                this.$refs.currentRowTable.clearCurrentRow();
            }
        }
    }
</script>
