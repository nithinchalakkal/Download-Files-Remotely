# Download Files Remotely



Sometimes you come across a file you want to download but all you've got is your smartphone. Perhaps it's a standard file, perhaps it's a torrent. Whatever the case may be, it's relatively simple to get your smartphone to tell your home computer to get started on that download from afar. Here's how.



# Procedure


1. Add Permission in Manifest
2. Add InstallAPK. Java class
3. Call InstallAPK class from Activity Class



# Extra Process [install downloaded APK Programmatically]

Intent intent = new Intent(Intent.ACTION_VIEW);
			intent.setDataAndType(
					Uri.fromFile(new File(sdcard,
							"Android/Downloadedfiles/Application.apk")),
							"application/vnd.android.package-archive");
							
							//Location along with Application name

			intent.setFlags(Intent.FLAG_ACTIVITY_NEW_TASK);
			context.startActivity(intent);
