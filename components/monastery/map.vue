<template>

  <div class="mt-5" style="background:#C9A081;">
    <div class="container">

      <div class="row" style="padding-top: 9rem;padding-bottom: 9rem;">
        <div class="col-md-6" style="padding-left: 3rem;padding-right: 3rem;">
          <iframe class="map"
                  :src="map.link"
                  width="100%" height="100%" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false"
                  tabindex="0">
          </iframe>
        </div>

        <div class="col-md-6">
          <div style="color:#ffffff;font-weight: bold;">
            <h5>แผนที่</h5>
          </div>

          <h6 class="pt-3" style="color:#ffffff;line-height: 1.6;">
            {{ (map.address) }}
          </h6>

          <div style="color:#ffffff;line-height: 1.6;">
            <h6 style="color: #8e4646;font-weight: bold;">เวลา เปิด,ปิด</h6>
            <div class="" style="padding-left: 3rem;">
              <table>
                <tr>
                  <td class="day">อาทิตย์</td>
                  <td>{{ (day.sunday) }}</td>
                </tr>
                <tr>
                  <td class="day">จันทร์</td>
                  <td>{{ (day.monday) }}</td>
                </tr>
                <tr>
                  <td class="day">อังคาร</td>
                  <td>{{ (day.tuesday) }}</td>
                </tr>
                <tr>
                  <td class="day">พุธ</td>
                  <td>{{ (day.wednesday) }}</td>
                </tr>
                <tr>
                  <td class="day">พฤหัสบดี</td>
                  <td>{{ (day.thursday) }}</td>
                </tr>
                <tr>
                  <td class="day">ศุกร์</td>
                  <td>{{ (day.friday) }}</td>
                </tr>
                <tr>
                  <td class="day">เสาร์</td>
                  <td>{{ (day.saturday) }}</td>
                </tr>
              </table>

            </div>

          </div>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: "map",
  props: {
    map: {
      type: Object,
      default: {
        link: "",
        address: "",
      }
    },
    day: {
      type: Object,
      default: {
        sunday: "",
        monday: "",
        tuesday: "",
        wednesday: "",
        thursday: "",
        friday: "",
        saturday: "",
      }
    }
  },
}
</script>

<style scoped>
.day {
  font-size: 1rem;
}

.history {
  font-weight: bold;
  color: #11174A;
}

.border-content {
  width: 100%;
  height: 0.7rem;
  background: rgb(238, 89, 38);
  background: linear-gradient(90deg, rgba(238, 89, 38, 1) 0%, rgba(59, 49, 133, 1) 50%, rgba(48, 47, 139, 1) 100%);
}
</style>
