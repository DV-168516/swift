add_swift_target_library(swiftOSLogPrototype
  IS_SDK_OVERLAY
  SHARED

  OSLog.swift
  OSLogMessage.swift
  OSLogIntegerFormatting.swift
  OSLogStringAlignment.swift
  OSLogIntegerTypes.swift
  OSLogStringTypes.swift
  OSLogNSObjectType.swift
  OSLogFloatingPointTypes.swift

  SWIFT_MODULE_DEPENDS_IOS Darwin os ObjectiveC
  SWIFT_MODULE_DEPENDS_OSX Darwin os ObjectiveC
  SWIFT_MODULE_DEPENDS_TVOS Darwin os ObjectiveC
  SWIFT_MODULE_DEPENDS_WATCHOS Darwin os ObjectiveC
  TARGET_SDKS ALL_APPLE_PLATFORMS
  SWIFT_COMPILE_FLAGS ${SWIFT_STANDARD_LIBRARY_SWIFT_FLAGS}
  INSTALL_IN_COMPONENT never_install
  DARWIN_INSTALL_NAME_DIR "${SWIFT_DARWIN_STDLIB_PRIVATE_INSTALL_NAME_DIR}")
