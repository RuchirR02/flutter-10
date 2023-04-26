# flutter-10
### fetch sync
self.addEventListener('push', function(event) {
    var data = event.data.json();
    event.waitUntil(
      self.registration.showNotification(data.title, {
        body: data.body,
        icon: data.icon
      })
    );
});

self.addEventListener('sync', function(event) {
    if (event.tag === 'my-sync') {
      event.waitUntil(
        // code to sync data with the server
      );
    }
});
