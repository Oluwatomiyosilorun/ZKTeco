<template>
  <div class="container_content">
    <div class="team_details mt-4 px-3">
      <section class="select">
        <form class="form-inline my-3">
          <select class="btn-top">
            <option>Select a team</option>
          </select>
        </form>

        <div>
          <p>Design Team</p>
          <div class="dought">
            <vc-donut
              background="#EEEEEE"
              foreground="white"
              :size="160"
              unit="px"
              :thickness="15"
              :sections="sections"
              :total="75"
              :start-angle="0"
              :auto-adjust-text-size="true"
            >
              <small>Time Log</small>
              <h1>65%</h1>
            </vc-donut>
          </div>
        </div>
      </section>

      <section class="projects mt-5">
        <div class="project_content">
          <p>Projects</p>

          <div class="project_boxes d-flex flex-wrap">
            <div class="box">
              <p class="title">Total</p>
              <div class="d-flex">
                <p class="total"></p>
                <p class="number">145</p>
              </div>
            </div>

            <div class="box">
              <p class="title">Completed</p>
              <div class="d-flex">
                <p class="completed"></p>
                <p class="number">115</p>
              </div>
            </div>

            <div class="box">
              <p class="title">In Progress</p>
              <div class="d-flex">
                <p class="in"></p>
                <p class="number">20</p>
              </div>
            </div>

            <div class="box">
              <p class="title">Waiting</p>
              <div class="d-flex">
                <p class="waiting"></p>
                <p class="number">10</p>
              </div>
            </div>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      sections: [
        { value: 65, color: "#5B6BFF" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.container_content {
  position: absolute;
  font-family: Nunito;
  width: 18%;
  height: 100vh;
  box-shadow: 0px 0px 17px rgba(8, 37, 100, 0.09);
  background: white;
  z-index: 1000;
  top: 10%;
  right: 0;
  .team_details {
    p {
      font-family: Nunito;
      font-style: normal;
      font-weight: 600;
      font-size: 18px;
      line-height: 25px;
      color: #001233;
    }
    select {
      font-style: normal;
      font-weight: 600;
      font-size: 16px;
      line-height: 22px;
      padding: 9px;
      border: none;
      width: 100%;
    }
    .projects {
      .project_content {
        .project_boxes {
          justify-content: space-between;
          .box {
            background: #f7f6fb;
            border-radius: 16px;
            width: 46%;
            margin-bottom: 8%;
            padding: 10% 3% 5% 5%;
            .title {
              font-style: normal;
              font-weight: normal;
              font-size: 11px;
              line-height: 140%;
              color: #898ca6;
              margin-bottom: 0;
              text-transform: uppercase;
            }
            .number {
              font-style: normal;
              font-weight: bold;
              font-size: 26px;
              line-height: 35px;
              color: #001233;
              margin-bottom: 0;
              margin-left: 5px;
            }
            .total {
              width: 3%;
              height: 22px;
              margin: auto 0;
              background: #e67a00;
            }
            .completed {
              width: 4%;
              height: 22px;
              margin: auto 0;
              background: #363ade;
            }
            .in {
              width: 3%;
              height: 22px;
              margin: auto 0;
              background: #10a237;
            }
            .waiting {
              width: 4%;
              height: 22px;
              margin: auto 0;
              background: #ff5041;
            }
          }
        }
      }
    }
  }
}
.dought {
  width: 180px;
  height: 180px;
  padding: 10px;
  background: #eeeeee;
  box-shadow: 2px 2px 2px 1px rgba(0, 0, 0, 0.09);
  border-radius: 50%;
  small{
    font-family: Graphik;
    font-style: normal;
    font-weight: normal;
    font-size: 15px;
    line-height: 17px;
    color: #9B9B9B;
  }
  h1{
    font-family: Graphik;
    font-style: normal;
    font-weight: normal;
    font-size: 20px;
    line-height: 22px;
    text-align: center;
    color: #121212;
  }
}
</style>