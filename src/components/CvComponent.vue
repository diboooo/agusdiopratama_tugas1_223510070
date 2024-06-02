<template>
  <div class="cv">
    <header>
      <h1>{{ name }}</h1>
      <p class="title">{{ title }}</p>
    </header>
    <section>
      <h2>Pengalaman</h2>
      <ul>
        <li v-for="job in experience" :key="job.id">
          <h3>{{ job.position }} - <span class="company">{{ job.company }}</span></h3>
          <p>{{ job.description }}</p>
        </li>
      </ul>
    </section>
    <section>
      <h2>Sekolah</h2>
      <ul>
        <li v-for="edu in education" :key="edu.id">
          <h3>{{ edu.degree }} - <span class="institution">{{ edu.institution }}</span></h3>
          <p>{{ edu.year }}</p>
        </li>
      </ul>
    </section>
    <section>
      <h2>Skill</h2>
      <ul class="skills-list">
        <li v-for="skill in skills" :key="skill.id">{{ skill }}</li>
      </ul>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'AgusDio Pratama',
      title: 'Si Ganteng :)',
      experience: [
        { id: 1, position: 'Sales Ardiles', company: 'Ardiles', description: 'Sales' },
        { id: 2, position: 'kasir', company: 'Fadillajayastore', description: 'Menjaga kasir' },
      ],
      education: [
        { id: 1, degree: 'SD 10 ATTS', institution: 'Sekolah Dasar', year: '6 Tahun' },
        { id: 2, degree: 'SMPN 6 BUKITINGGI', institution: 'NEGRI', year: '3 Tahun' },
        { id: 2, degree: 'SMKN 1 BUKITTINGI', institution: 'NEGRI', year: '3 Tahun' },
      ],
      skills: ['BUBUT', 'CNC', 'GAMER'],
    };
  },
};
</script>

<style scoped>
.cv {
  font-family: 'Helvetica Neue', Arial, sans-serif;
  max-width: 800px;
  margin: 40px auto;
  padding: 20px;
  border: 1px solid #ddd;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  background-color: #0f0000;
}

header {
  text-align: center;
  margin-bottom: 20px;
}

h1 {
  font-size: 2.5em;
  margin-bottom: 0.2em;
  color: #333;
}

.title {
  font-size: 1.2em;
  color: #777;
}

h2 {
  color: #0056b3;
  border-bottom: 2px solid #0056b3;
  padding-bottom: 5px;
  margin-bottom: 10px;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  margin-bottom: 15px;
}

h3 {
  font-size: 1.1em;
  margin-bottom: 5px;
}

.company, .institution {
  color: #0056b3;
  font-weight: bold;
}

.skills-list {
  display: flex;
  flex-wrap: wrap;
}

.skills-list li {
  background-color: #f0f0f0;
  border: 1px solid #ddd;
  border-radius: 5px;
  padding: 5px 10px;
  margin: 5px;
}
</style>
