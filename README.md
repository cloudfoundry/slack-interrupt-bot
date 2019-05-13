Configuration for the `@interrupt` bot in [cloudfoundry.slack.com](slack.cloudfoundry.org).

 * running with [dpb587/slack-delegate-bot](https://github.com/dpb587/slack-delegate-bot)
 * deployed on [Pivotal Web Services](https://run.pivotal.io/)

To add new behavior, send a pull request.

---

    fly -t "$FLY_TARGET" set-pipeline \
      --pipeline cloudfoundry-slack-interrupt-bot \
      --config ~/workspace/src/github.com/dpb587/slack-delegate-bot/examples/cf-app/concourse.yml \
      --load-vars-from <( lpass show --notes "github.com/dpb587/cloudfoundry-slack-interrupt-bot//vars.yml" )
