<template>
 <div>
          <div class="admin">
            <div class="cards flex">
                <div class="card c1">
                    <div class="top flex">
                        <div class="stat">
                            <h1>50</h1>
                            <span>New Orders</span>
                        </div>
                        <div class="icon">
                            <span class="el-icon-menu"></span>
                        </div>
                    </div>
                </div>
                <div class="card c2">
                    <div class="top flex">
                        <div class="stat">
                            <h1>50</h1>
                            <span>New Orders</span>
                        </div>
                        <div class="icon">
                                  <span class="el-icon-menu"></span>
                        </div>
                    </div>
                </div>
                <div class="card c3">
                    <div class="top flex">
                        <div class="stat">
                            <h1>50</h1>
                            <span>New Orders</span>
                        </div>
                        <div class="icon">      <span class="el-icon-menu"></span></div>
                    </div>
                </div>
                <div class="card c4">
                    <div class="top flex">
                        <div class="stat">
                            <h1>50</h1>
                            <span>New Orders</span>
                        </div>
                        <div class="icon">      <span class="el-icon-menu"></span></div>
                    </div>
                </div>
            </div>
        </div>
        <div class="table-data">

        <div class="title-box-top">
        <div class="title-top-left">
          <h4 class="title-page">Barcha haydovchilar</h4>
        </div>

        <div class="title-box-right flex">
          <!-- <div class="export">
            <el-button size="medium" class="bg-btn" @click="openModalAdd">
              <i class="el-icon-download"></i> Export</el-button
            >

           
          </div> -->
         
        </div>
      </div>
      <div class="table">
        <table v-if="tableData1 != null">
          <thead>
            <tr>
              <th>#</th>
              <th>F.I.O</th>
              <th>Telefon:</th>
              <th>Guruhi</th>
              <th>Ta'lim turi</th>
              <th>Status</th>
              <th></th>
            </tr>
          </thead>
          <tbody>
            <tr
              style="border-bottom: 1px solid"
              v-for="(item, index) in tableData1"
              :key="item"
            >
              <td>{{ index + 1 }}</td>
              <td>
                <div class="name"></div>
                {{ item.name }}
              </td>
              <td>
                <div class="name"></div>
                {{ item.tel }}
              </td>
              <td>
                {{ item.group }}
              </td>
              <td>
                <div class="name"></div>
                {{ item.type }}
              </td>
              <td>
                <div v-if="item.oplata" class="name">
                  <span class="true"> Faol </span>
                </div>
                <div v-if="item.oplata == false" class="name">
                  <span class="false"> Faolmas </span>
                </div>
              </td>
              <td>
                <div class="table-actions">
                  <el-button
                    @click="openModalEdit(item._id)"
                    type="primary"
                    icon="el-icon-edit"
                    size="mini"
                    plain
                    class="edit"
                  ></el-button>

                  <el-popconfirm
                    title="Ma`lumotni o'chirmoqchimisiz?"
                    confirm-button-text="Ha"
                    cancel-button-text="Yo'q"
                    cancel-button-type="danger"
                    @confirm="confirmDelete(item._id)"
                  >
                    <el-button
                      slot="reference"
                      type="danger"
                      icon="el-icon-delete"
                      size="mini"
                      plain
                    ></el-button>
                  </el-popconfirm>
                </div>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
        </div>

     
 </div>
</template>

<script>
export default { 
    layout: 'admin',
    
    data(){
        return{
             tableData1: [
        {
          name: "Xushnudbek Ayitboyev",
          year: 1998,
          tel: 9998900366009,
          type: "online",
          guruhi: "Matematika",
          group: 101,
          oplata: true,
          img: {
            id: 1232312,
            path: "as",
          },
        },
        {
          name: "Xushnudbek Ayitboyev",
          year: 1998,
          tel: 9998900366009,
          type: "online",
          guruhi: "Matematika",
          oplata: true,
          group: 101,
          img: {
            id: 1232312,
            path: "as",
          },
        },
        {
          name: "Xushnudbek Ayitboyev",
          year: 1998,
          tel: 9998900366009,
          type: "online",
          group: 101,
          guruhi: "Matematika",
          oplata: false,
          img: {
            id: 1232312,
            path: "as",
          },
        },
        {
          name: "Xushnudbek Ayitboyev",
          year: 1998,
          tel: 9998900366009,
          type: "online",
          group: 101,
          guruhi: "Matematika",
          oplata: true,
          img: {
            id: 1232312,
            path: "as",
          },
        },
        {
          name: "Xushnudbek Ayitboyev",
          year: 1998,
          tel: 9998900366009,
          type: "online",
          group: 101,
          guruhi: "Matematika",
          oplata: false,
          img: {
            id: 1232312,
            path: "as",
          },
        },
      ],
        }
        },
    }
</script>

<style lang="scss" scoped>
.table-data{
    background: #fff;
    padding: 20px;
    box-shadow: 0 4px 10px hsl(0deg 0% 92% / 30%);
    border-radius: 10px;
}
.title-page{
    font-size: 22px;
    margin-bottom: 0;
    color: #333;
}
    
.admin {
    margin-bottom: 20px;
    .info {
        margin-bottom: 20px;
    }
    .card {
        border-radius: 5px;
        padding: 15px;
        width: calc((100% - 80px) / 4);
        .top {
            .stat {
                h1 {
                    margin: 0 !important;
                    color: #fff;
                    font-size: 38px;
                }
                span {
                    color: #fff;
                }
            }
            .icon{
                // padding-right: 15px;
                span{
                    color: #fff;
                    font-size: 70px;
                }
            }
        }
    }
    .c1 {
        background-color: #00c0ef !important;
    }
    .c2 {
        background-color: #00a65a !important;
    }
    .c3 {
        background-color: #f39c12 !important;
    }
    .c4 {
        background-color: #dd4b39 !important;
    }
}
</style>
