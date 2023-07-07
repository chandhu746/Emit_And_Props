<template>
    <div class="data-display">
      <h2>Form Data Display</h2>
      <div v-if="formData">
        <p><strong>Name:</strong> {{ formData.name }}</p>
        <p><strong>Roll:</strong> {{ formData.roll }}</p>
        <p><strong>Email:</strong> {{ formData.email }}</p>
        <p><strong>Gender:</strong>{{ formData.gender }}</p>
        <p><strong>Phone:</strong>{{ formData.phone }}</p>
        <p><strong>Marks:</strong>{{ formData.marks }}</p>
        <p><strong>Hobbies:</strong>{{ formData.hobbies.join(',') }}</p>
      </div>
    </div>
    
  </template>
  
  <script lang="ts">
  export default {
    props: {
      formData: {
        type: Object as () => FormDataInterface,
        required: true
      }
    }
  };

  interface FormDataInterface {
  name: string;
  roll: string;
  email: string;
  gender: string;
  phone: string;
  marks: number;
  hobbies: string[];
}
  </script>


<style>
.data-display {
  max-width: 400px;
  margin: 0 auto;
  padding: 20px;
  background-color: black;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.data-display h2 {
  margin-bottom: 10px;
}

.data-display p {
  margin: 5px 0;
}

.data-display strong {
  font-weight: bold;
}

</style>