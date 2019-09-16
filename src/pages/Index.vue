<template>
  <q-page class="flex flex-center">
    <img alt="Quasar logo" src="~assets/quasar-logo-full.svg">
    hello
    {{ test }}
  </q-page>
</template>

<style>
</style>

<script>
// const USER = 'tcardlab'
// const PASS = 'TCLab2@71828'
// const REPO = 'github.com/tcardlab/Js-git-test'

// var git = require('simple-git/promise')
// const remote = `https://${USER}:${PASS}@${REPO}`

// simpleGit().clone(remote)

/* const git = require('simple-git')
const path = '..'

git(path).raw([
  'config',
  '--global',
  'advice.pushNonFastForward',
  'false'
]) */

/* git().ChildProcess.spawn = (function () {
  var cachedSpawn = require('child_process').spawn
  return function () {
    var args = ['sudo', [arguments['0']]]
    var keys = Object.keys(arguments)
    if (keys.length >= 2 && arguments['1'].length != null) {
      args[1] = args[1].concat(arguments['1'])
    }
    if (keys.length >= 3) {
      args.push(arguments['2'])
    }
    var result = cachedSpawn.apply(this, args)
    return result
  }
})() */

/* git().clone(remote)
  .then(() => console.log('finished'))
  .catch((err) => console.error('failed: ', err)) */

/* require('simple-git')()
  .listRemote(['--get-url'], (err, data) => {
    if (!err) {
      console.log('Remote url for repository at ' + __dirname + ':');
      console.log(data);
    }
  }); */

export default {
  name: 'PageIndex',
  computed: {
    test () {
      return false // simpleGit.status
    }
  }
}
</script>
