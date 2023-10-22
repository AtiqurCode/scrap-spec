<template>
  <div class="relative flex flex-col rounded-xl bg-transparent bg-clip-border text-gray-700 shadow-none">
    <h4 class="block font-sans text-2xl font-semibold leading-snug tracking-normal text-blue-gray-900 antialiased">
      Scrap data from html code to table data
    </h4>
    <form class="mt-8 mb-2 w-100 max-w-screen-lg sm:w-200" @submit.prevent="submitForm">
      <div class="mb-4 flex flex-col gap-6">
        <div class="relative w-full min-w-[200px]">
      <textarea
        rows="8"
        class="block p-2.5 w-full text-sm text-gray-900 bg-gray-50 rounded-lg border border-gray-300 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
        placeholder="Paste your html code here"
        v-model="formData.scrapCode"
      ></textarea>
      <!-- <label class="before:content[' '] after:content[' '] pointer-events-none absolute left-0 -top-1.5 flex h-full w-full select-none text-[11px] font-normal leading-tight text-blue-gray-400 transition-all before:pointer-events-none before:mt-[6.5px] before:mr-1 before:box-border before:block before:h-1.5 before:w-2.5 before:rounded-tl-md before:border-t before:border-l before:border-blue-gray-200 before:transition-all after:pointer-events-none after:mt-[6.5px] after:ml-1 after:box-border after:block after:h-1.5 after:w-2.5 after:flex-grow after:rounded-tr-md after:border-t after:border-r after:border-blue-gray-200 after:transition-all peer-placeholder-shown:text-sm peer-placeholder-shown:leading-[3.75] peer-placeholder-shown:text-blue-gray-500 peer-placeholder-shown:before:border-transparent peer-placeholder-shown:after:border-transparent peer-focus:text-[11px] peer-focus:leading-tight peer-focus:text-blue-500 peer-focus:before:border-t-2 peer-focus:before:border-l-2 peer-focus:before:border-blue-500 peer-focus:after:border-t-2 peer-focus:after:border-r-2 peer-focus:after:border-blue-500 peer-disabled:text-transparent peer-disabled:before:border-transparent peer-disabled:after:border-transparent peer-disabled:peer-placeholder-shown:text-blue-gray-500">
        Paste your html code here
      </label> -->
    </div>
      </div>
      <button
        class="mt-6 block w-full select-none rounded-lg bg-blue-500 py-3 px-6 text-center align-middle font-sans text-xs font-bold uppercase text-white shadow-md shadow-blue-500/20 transition-all hover:shadow-lg hover:shadow-blue-500/40 focus:opacity-[0.85] focus:shadow-none active:opacity-[0.85] active:shadow-none disabled:pointer-events-none disabled:opacity-50 disabled:shadow-none"
        type="submit"
        data-ripple-light="true"
      >
        Scrap code to html table data
      </button>
      <p class="mt-4 block text-center font-sans text-base font-normal leading-relaxed text-gray-700 antialiased">
        Gallary Gadgets web url
        <a
          class="font-medium text-blue-500 transition-colors hover:text-blue-700"
          href="https://gallarygadgets.com/"
        >
          Click here
        </a>
      </p>
    </form>

    <div class="w-100 pt-8" v-if="scrapTableData">
      <div class="relative w-full min-w-[200px] pb-6">
        <textarea
          rows="8"
          class="block p-2.5 w-full text-sm text-gray-900 bg-gray-50 rounded-lg border border-gray-300 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500"
          placeholder="Scrap table data"
          v-model="scrapTableData"
        ></textarea>

        <button
          class="mt-6 block w-full select-none rounded-lg bg-blue-500 py-3 px-6 text-center align-middle font-sans text-xs font-bold uppercase text-white shadow-md shadow-blue-500/20 transition-all hover:shadow-lg hover:shadow-blue-500/40 focus:opacity-[0.85] focus:shadow-none active:opacity-[0.85] active:shadow-none disabled:pointer-events-none disabled:opacity-50 disabled:shadow-none"
          type="submit"
          data-ripple-light="true"
          @click="copyToClipboard"
        >
          Copy table data
        </button>
        <!-- <label class="before:content[' '] after:content[' '] pointer-events-none absolute left-0 -top-1.5 flex h-full w-full select-none text-[11px] font-normal leading-tight text-blue-gray-400 transition-all before:pointer-events-none before:mt-[6.5px] before:mr-1 before:box-border before:block before:h-1.5 before:w-2.5 before:rounded-tl-md before:border-t before:border-l before:border-blue-gray-200 before:transition-all after:pointer-events-none after:mt-[6.5px] after:ml-1 after:box-border after:block after:h-1.5 after:w-2.5 after:flex-grow after:rounded-tr-md after:border-t after:border-r after:border-blue-gray-200 after:transition-all peer-placeholder-shown:text-sm peer-placeholder-shown:leading-[3.75] peer-placeholder-shown:text-blue-gray-500 peer-placeholder-shown:before:border-transparent peer-placeholder-shown:after:border-transparent peer-focus:text-[11px] peer-focus:leading-tight peer-focus:text-blue-500 peer-focus:before:border-t-2 peer-focus:before:border-l-2 peer-focus:before:border-blue-500 peer-focus:after:border-t-2 peer-focus:after:border-r-2 peer-focus:after:border-blue-500 peer-disabled:text-transparent peer-disabled:before:border-transparent peer-disabled:after:border-transparent peer-disabled:peer-placeholder-shown:text-blue-gray-500">
          Here is you html table data
        </label> -->
      </div>


      <div id="toast-success" v-if="alertSuccess" class="flex items-center w-full min-w-[200px] p-4 mb-4 text-gray-500 bg-white rounded-lg shadow dark:text-gray-400 dark:bg-gray-800" role="alert">
          <div class="inline-flex items-center justify-center flex-shrink-0 w-8 h-8 text-green-500 bg-green-100 rounded-lg dark:bg-green-800 dark:text-green-200">
              <svg class="w-5 h-5" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 20 20">
                  <path d="M10 .5a9.5 9.5 0 1 0 9.5 9.5A9.51 9.51 0 0 0 10 .5Zm3.707 8.207-4 4a1 1 0 0 1-1.414 0l-2-2a1 1 0 0 1 1.414-1.414L9 10.586l3.293-3.293a1 1 0 0 1 1.414 1.414Z"/>
              </svg>
              <span class="sr-only">Check icon</span>
          </div>
          <div class="ml-3 text-sm font-normal">Copy the html table data successfully.</div>
          <button type="button" @click="alertToast" class="ml-auto -mx-1.5 -my-1.5 bg-white text-gray-400 hover:text-gray-900 rounded-lg focus:ring-2 focus:ring-gray-300 p-1.5 hover:bg-gray-100 inline-flex items-center justify-center h-8 w-8 dark:text-gray-500 dark:hover:text-white dark:bg-gray-800 dark:hover:bg-gray-700" data-dismiss-target="#toast-success" aria-label="Close">
              <span class="sr-only">Close</span>
              <svg class="w-3 h-3" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 14 14">
                  <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="m1 1 6 6m0 0 6 6M7 7l6-6M7 7l-6 6"/>
              </svg>
          </button>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import cheerio from 'cheerio';

let scrapTableData = ref(null);
const alertSuccess = ref(false);
const div_p_value = ref('');

const formData = ref({
  scrapCode: ''
});

const submitForm = () => { 
  const productSpeec = formData.value.scrapCode;


  const $ = cheerio.load(productSpeec);
  const tableData = {};

  if($('p').text() != '')
    div_p_value.value = `<p><em><span style="color: #616161;">${$('p').text()}</span></em></p>`;

  // Iterate over each table and extract data
  $('table').each((index, element) => {
    const rows = $(element).find('tr');
    const category = $(rows[0]).find('th').text().trim();
    const categoryData = {};


    // Iterate over rows and extract key-value pairs
    rows.each((i, row) => {
      const key = $(row).find('.ttl').text().trim();
      const value = $(row).find('.nfo').text().trim();
      if (key == '') {
        const keys = Object.keys(categoryData);
        const lastKey = keys.pop();
        const lastValue = categoryData[lastKey];
        categoryData[lastKey] = lastValue + ' <br> ' + value;
      } else {
        categoryData[key] = value;
      }
    });

    // Add category data to the main object
    tableData[category] = categoryData;
  });

  // Convert the extracted data to JSON format
  const data = JSON.stringify(tableData, null, 2);
  const jsonData = JSON.parse(data);
  // console.log(jsonData);

  scrapTableData.value = generateHTMLFromJSON(jsonData);

};

function generateHTMLFromJSON(jsonData) {
  let html = '';

  if(div_p_value.value != '')
    html += div_p_value.value;

  for (const section in jsonData) {
    html += `<h2><span style="color: #1770dc;">${section}</span></h2><table><tbody>`;
    const sectionData = jsonData[section];

    for (const key in sectionData) {
      let value = sectionData[key];

      if (value == "No")
        value = '❌';
      if (value == "Yes")
        value = '✅';

      html += `<tr><td><strong><span style="color: #616161;">${key}</span></strong></td><td>${value}</td></tr>`;

    }

    html += `</tbody></table>`;
  }

  html += `<p><span style="color: #616161;"><em><strong>Disclaimer:</strong> We cannot guarantee that the information on this page is 100% accurate.  Please help us if you have found any mistake or wrong information.</span></em></p>`;

  return html;
}


const copyToClipboard = () => {
  const textarea = document.createElement('textarea');
  textarea.value = scrapTableData.value;
  document.body.appendChild(textarea);
  textarea.select();
  document.execCommand('copy');
  document.body.removeChild(textarea);
  alertSuccess.value = true;
}

const alertToast = () => {
  alertSuccess.value = false;
}
</script>