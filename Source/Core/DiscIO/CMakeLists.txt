add_library(discio
  Blob.cpp
  Blob.h
  CISOBlob.cpp
  CISOBlob.h
  CompressedBlob.cpp
  CompressedBlob.h
  DirectoryBlob.cpp
  DirectoryBlob.h
  DiscExtractor.cpp
  DiscExtractor.h
  DiscScrubber.cpp
  DiscScrubber.h
  Enums.cpp
  Enums.h
  FileBlob.cpp
  FileBlob.h
  FileSystemGCWii.cpp
  FileSystemGCWii.h
  Filesystem.cpp
  Filesystem.h
  NANDImporter.cpp
  NANDImporter.h
  TGCBlob.cpp
  TGCBlob.h
  Volume.cpp
  Volume.h
  VolumeFileBlobReader.cpp
  VolumeFileBlobReader.h
  VolumeGC.cpp
  VolumeGC.h
  VolumeVerifier.cpp
  VolumeVerifier.h
  VolumeWad.cpp
  VolumeWad.h
  VolumeWii.cpp
  VolumeWii.h
  WbfsBlob.cpp
  WbfsBlob.h
  WiiSaveBanner.cpp
  WiiSaveBanner.h
)

if(NOT IOS)
  target_sources(discio PRIVATE
    DriveBlob.cpp
    DriveBlob.h
  )
endif()

target_link_libraries(discio
PRIVATE
  minizip
  pugixml
  ZLIB::ZLIB
)
