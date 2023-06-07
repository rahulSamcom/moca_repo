# Uncomment the next line to define a global platform for your project
# platform :ios, '9.0'

target 'MocaDC' do
  # Comment the next line if you don't want to use dynamic frameworks
  use_frameworks!

  pod 'ObjectMapper'
  post_install do |installer|
    installer.generated_projects.each do |project|
      project.targets.each do |target|
        target.build_configurations.each do |config|
          config.build_settings['IPHONEOS_DEPLOYMENT_TARGET'] = '12.0'
          config.build_settings['SWIFT_SUPPRESS_WARNINGS'] = "YES"
          config.build_settings['GCC_WARN_INHIBIT_ALL_WARNINGS'] = "YES"
        end
      end
    end
    installer.pods_project.build_configurations.each do |config|
        config.build_settings['CLANG_WARN_QUOTED_INCLUDE_IN_FRAMEWORK_HEADER'] = "NO"
    end
  end
  
end
