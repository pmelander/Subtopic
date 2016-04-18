Subtopic provides topic-based PubSub for javascript. Originally based on Peter Higgins' port from Dojo to JQuery and updated with support for message chaining inspired by Morgan Roderick's PubSubJS.

Full documentation here: http://pmelander.github.com/Subtopic/

Vanilla javascrip:
subtopic.subscribe(topic, callback);
subtopic.unsubscribe(topic);
subtopic.publish(topic, [payload]);

Underscore:
_.subscribe(topic, callback);
_.unsubscribe(topic);
_.publish(topic, [payload]);

jQuery:
$.subscribe(topic, callback);
$.unsubscribe(topic);
$.publish(topic, [payload]);

Performance:
Check out the official performance comparison here:
http://jsperf.com/pubsubjs-vs-jquery-custom-events/50

Topic chaining:
To use topic chaining divide your topics using forward slashes e.g. app/region/module/event
A subscriber will execute the callback function for the subscribed topic and any sub-topics.

The following publications will each invoke the callback for a subscription to app/region:
_.publish("app/region", []);
_.publish("app/region/module", []);
_.publish("app/region/module/event", []);

