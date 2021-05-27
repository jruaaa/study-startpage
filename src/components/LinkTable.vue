<template>
<table class="table-auto w-full text-sm">
    <tr>
        <td><b>Read</b></td>
        <Link url="https://misd.schoology.com" name="schoology"/>
        <Link url="http://family.mercerisland.wa-k12.net/" name="skyward"/>
    </tr>
    <tr>
        <td><b>Write</b></td>
        <Link url="https://docs.google.com" name="google docs"/>
        <Link url="https://drive.google.com" name="google drive"/>
    </tr>
    <tr>
        <td><b>Class Links</b></td>
        <Link url="https://mercerislandschools.zoom.us/j/95429474860" name="P1"/>
        <Link url="https://mercerislandschools.zoom.us/j/85787280330" name="P3"/>
        <Link url="https://mercerislandschools.zoom.us/j/93305194723?pwd=RjF0a2hDQzlUd3FqTzgwdU5IMDZwZz09" name="P7"/>
        <Link url="https://mercerislandschools.zoom.us/j/98281543560" name="P2"/>
        <Link url="https://mercerislandschools.zoom.us/j/91010712635" name="Islander Hour"/>
        <Link url="https://mercerislandschools.zoom.us/j/96765745509" name="P4"/>
        <Link url="https://mercerislandschools.zoom.us/j/96754655426?pwd=eFVKZzVhYk9TaHVQdHJMKzNMR3piZz09" name="P6"/>
    </tr>
</table>
</template>

<script>
import Link from './Link.vue';

export default {
  name: 'LinkTable',
  components: { Link },
};
</script>
