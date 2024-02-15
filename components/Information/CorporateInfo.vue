<template>
    <v-container fluid>
        <v-card class="pa-6" elevation="5">
            <v-card-text>
                <div v-for="item in items">
                    <v-row>
                        <v-col cols="3" class="my-auto mr-10 text-right">{{ item.title }}</v-col>
                        <v-col class="pa-4" v-html="item.content" />
                    </v-row>
                    <v-divider class="my-4" />
                </div>
                <v-row>
                    <v-col cols="3" class="mr-10 my-auto text-right">業務内容</v-col>
                    <v-col class="pa-4">
                        <ul>
                            <li v-for="work in works">{{ work }}</li>
                        </ul>
                    </v-col>
                </v-row>
            </v-card-text>
        </v-card>
    </v-container>
</template>

<script setup lang="ts">
interface TableItem {
    title: string
    content: string
}

const items: TableItem[] = [
    {
        title: "社名",
        content: "合同会社ランベージ（Lambuage LLC）"
    },
    {
        title: "所在地",
        content: "〒530-0001<br />大阪府大阪市北区梅田1丁目2番2号大阪駅前第2ビル12-12"
    },
    {
        title: "資本金",
        content: "100万円"
    },
    {
        title: "代表社員",
        content: "石田 慎介"
    },
    {
        title: "設立",
        content: "2024年1月"
    },
]

const works: string[] = [
    "翻訳、通訳に関する手配、ディレクション及びコンサルテイング業務",
    "コンビュータのソフトウェア及びハードウェアの企画、研究、開発、設計、製造、販売、保守、リース、賃貸、輸出入並びにそれらに関するコンサルティング業務",
    "コンピュータシステムによるデータ入力及びそれに伴う事移処理の受託",
    "コンピュータの操作指導等に関する事業",
    "インターネット等の通信ネットワーク及び電子技術を利用した各種情報提供サービス、情報収集サービス",
    "情報の収集、分析、管理及び処理サービス業、情報提供サービス業並びに情報処理に関する研究開発",
    "人材の育成、職業適性、能力開発のための教育及びカウンセリング業務",
    "各種勉強会の開催、会員間の情報交換及び相互交流の実施",
    "スクール、サロン等の経営及び開設指導",
    "EC (電子商取引)サイト、その他各種ウェブサイトの画、制作、販売、配信、運営及び管理",
    "各種商品の企画、製造、販売及び輸出入",
    "前各号に附帯関連する一切の事業"
]
</script>