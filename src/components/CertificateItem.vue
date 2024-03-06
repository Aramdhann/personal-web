<template>
  <section class="container certificate">
    <h1>Certification & Competition</h1>
    <div class="certif-list">
      <div class="card-base-animate">
        <div class="card card-animate">
          <div class="card-content">
            <div class="card-header">
              <img src="../assets/images/certif.png" alt="certification" />
              <div>
                <p class="certif-title">Title Certification</p>
                <p>by company name</p>
              </div>
            </div>
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit.
              Assumenda, at dicta quia nesciunt nulla magni voluptate dolorem ab
              labore provident perferendis quas nemo, sed veritatis fugit
              tenetur eos enim quisquam?
              <a class="text-link">Read more</a>
            </p>
            <div class="card-tag-list">
              <div class="card-tag">Certified at 19-12-2023</div>
              <div class="card-tag">Due to 19-12-2023</div>
            </div>
          </div>
        </div>
      </div>
      <div class="competition">
        <div class="card-base-animate">
          <div class="card card-animate">
            <div class="card-content">
              <div class="card-header">
                <img
                  class="icon-compe"
                  src="../assets/images/compe.png"
                  alt="competition"
                />
                <div>
                  <p class="certif-title">Title Certification</p>
                  <p>by company name</p>
                </div>
              </div>
              <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
                Assumenda, at dicta quia nesciunt nulla magni voluptate dolorem
                ab labore provident perferendis quas nemo, sed veritatis fugit
                tenetur eos enim quisquam?
                <a class="text-link">Read more</a>
              </p>
              <div class="card-tag-list">
                <div class="card-tag">Certified at 19-12-2023</div>
                <div class="card-tag">Due to 19-12-2023</div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<style>
.certif-list {
  display: flex;
  gap: 10px;
  overflow-x: auto;
  padding: 15px 0;
}

.certificate {
  padding: 115px 0px;
}

.competition img {
  width: 40px;
}

.certif-list .card {
  max-height: 300px;
}

@media (max-width: 876px) {
  .certificate {
    padding: 80px 0;
  }
}
</style>
