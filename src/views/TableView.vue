<template>
  <body>
    <header>
      <div class="header-wrapper">
        <ul>
          <li id="order">
            <font-awesome-icon
              :icon="['fas', 'receipt']"
              :style="{ color: 'black' }"
            />
            접수
          </li>
          <li id="order-list">
            <font-awesome-icon
              :icon="['fas', 'list']"
              :style="{ color: 'blue' }"
            />
            주문목록
          </li>
          <li id="logout">
            <font-awesome-icon
              :icon="['fas', 'arrow-right-from-bracket']"
              :style="{ color: 'black' }"
            />
            로그아웃
          </li>
        </ul>
        <div class="user-container">
          <font-awesome-icon
            :icon="['fas', 'user']"
            class="user-icon"
            :style="{ color: 'black' }"
          />
        </div>
      </div>
    </header>

    <div class="body-container">
      <div class="input-container">
        <div>
          <input type="text" id="date-txt" value="2023-12-18 ~ 2024-01-12" />
        </div>
        <div class="search-container">
          <input type="text" id="search-txt" />
          <input type="submit" value="검색" id="search-btn" />
          <div class="button-container">
            <input type="submit" value="주문" id="order-btn" />
            <input type="submit" value="삭제" id="delete-btn" />
          </div>
        </div>
      </div>

      <div class="table-container">
        <table>
          <th><input type="checkbox" /></th>
          <th>업체ID</th>
          <th>업태</th>
          <th>업체몀</th>
          <th>환자명</th>
          <th>종류</th>
          <th>치식</th>
          <th>접수일시</th>
          <th>상태</th>
          <th>배송일시</th>
          <th>비고</th>
          <th>Scan</th>
          <th>Modeling</th>
          <th>Zip</th>
          <tr v-for="(item, index) in items" :key="index">
            <td><input type="checkbox" /></td>
            <td>DE0001</td>
            <td>치과의원</td>
            <td>A치과</td>
            <td>A씨</td>
            <td>A</td>
            <td>{{ item.index }}</td>
            <td>2023.11.30 14:24:30</td>
            <td>작성완료</td>
            <td>2023.11.31 08:24:12</td>
            <td></td>
            <td><font-awesome-icon :icon="['fas', 'download']" /></td>
            <td><font-awesome-icon :icon="['fas', 'download']" /></td>
            <td><font-awesome-icon :icon="['fas', 'download']" /></td>
          </tr>
        </table>
      </div>
    </div>
  </body>
</template>
<style>
header {
  width: 100%;
  margin: 0px;
  left: 50%;
  position: absolute;
  transform: translate(-50%, 0);
  display: flex;
  justify-content: space-between;
  border-bottom: solid 1px;
}

header ul {
  display: flex;
  text-align: center;
  margin-left: 40px;
}

#order-list {
  color: #0040ff;
}

header ul li {
  margin-right: 30px;
  list-style-type: none;
}
.header-wrapper {
  display: flex;
  justify-content: space-between;
  width: 100%;
  margin-top: 20px;
  margin-bottom: 20px;
}
.user-icon {
  height: 20px;
}
.user-container {
  padding: 0px 40px 0px 40px;
}

.body-container {
  background: #fff;
  margin: 0px;
  width: 95%;
  height: auto;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  /* border: 1px solid #d6d6d6; */
  padding: 30px;
}
.table-container table {
  width: 100%;
  height: 100%;
  text-align: center;
  border-collapse: collapse;
}
.table-container table th {
  border-bottom: 1px solid #444444;
  padding: 15px;
}
.table-container table tr {
  border-bottom: 1px solid #444444;
  padding: 15px;
}
.table-container table tr td {
  padding: 20px;
}
.input-container {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: space-between;
  margin-bottom: 30px;
}
.button-container {
  margin-top: 20px;
  display: flex;
  justify-content: flex-end;
}
.search-container {
  width: auto;
}

.input-container input[type="text"] {
  margin-right: 20px;
  width: 250px;
  height: 40px;
  padding: 0 10px;
  box-sizing: border-box;
  border-radius: 6px;
  background-color: #f8f8f8;
  border: 1px solid;
}
.search-container input[type="submit"] {
  background: #fff;
  width: 60px;
  height: 40px;
  border-radius: 6px;
  font-size: 15px;
}
#order-btn {
  margin-right: 20px;
  border: solid 1px #0040ff;
  color: #0040ff;
}
#delete-btn {
  border: solid 1px #ff0000;
  color: #ff0000;
}
#search-btn {
  border: solid 1px;
}
</style>
<script setup>
import { ref } from "vue";

const items = ref([
  {
    index: "13",
  },
  {
    index: "14",
  },
  {
    index: "1",
  },
  {
    index: "15",
  },
  {
    index: "21",
  },
  {
    index: "20",
  }
]);
</script>