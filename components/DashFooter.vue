<template>
    <!-- Main footer -->
    <footer class="flex items-center justify-between p-4 bg-white border-t dark:bg-darker dark:border-primary-darker">
        <div>Organic Shop © {{year}}</div>
        <!-- <div>
            Made by
            <a href="https://github.com/Kamona-WD" target="_blank" class="text-blue-500 hover:underline">Ahmed Kamel</a>
        </div> -->
    </footer>
</template>
<script>
  export default {
   data(){
      return {
          year: new Date().getFullYear()
      }
    }
  }
</script>
