<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="environment-reprovision.md" target-language="ar-SA">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>environment-reprovision.33170a.795ff0c91f6e5c2ac83dd610a125d2f6fdbbec70.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>795ff0c91f6e5c2ac83dd610a125d2f6fdbbec70</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\includes\environment-reprovision.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101">
          <source>When copying a database between environments, you will need to run the environment re-provisioning tool before the copied database is fully functional, to ensure that all Retail components are up-to-date.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">عند نسخ قاعدة بيانات بين البيئات، ستحتاج إلى تشغيل أداة إعادة تزويد البيئة قبل أن تصبح قاعدة البيانات المنسوخة قادرة على أداء وظائفها بشكل كامل، لكي تتأكد من أن جميع مكونات Retail محدّثة.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102">
          <source>We recommend that you run this procedure whether you are using Retail components or not, because Retail functionality is included in all environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">نوصي بتشغيل هذا الاجراء سواء كنت تستخدم مكونات Retail أم لا، لأن وظائف Retail مضمنة في كافة البيئات.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Before you continue, you must make sure that the following prerequisites are met:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">قبل المتابعة، يجب التأكد من استيفاء المتطلبات الأساسية التالية:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>If you are upgrading to the July 2017 release (also known as 7.2) 7.2.11792.56024, apply the following application X++ hotfixes in the destination environment before running the data upgrade in that environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">إذا كنت تقوم بالترقية إلى الإصدار 7.2.11792.56024 لشهر يوليو 2017 (يعرف أيضًا بالإصدار 7.2)، فطبّق الإصلاحات العاجلة X++ التالية للتطبيق على البيئة الوجهة قبل تشغيل ترقيه البيانات في تلك البيئة.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>These will prevent various errors occurring during the data upgrade:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ستؤدي هذه الإصلاحات إلى منع حدوث أخطاء متنوعة أثناء ترقيه البيانات:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>KB 4036156 - Retail minor version upgrade - 'Variant number sequence is not set.'</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KB 4036156 - ترقية إصدار ثانوي من Retail - '‏‫لم يتم تعيين التسلسل الرقمي للمتغير.‬'</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This fix package also includes KB 4035399 and KB 4035751.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">تتضمن حزمة الإصلاحات هذه KB 4035399 وKB 4035751.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Note that you must have a minimum of Platform Update 9 to use this package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">من الضروري أن يتوفر Platform Update 9 كحدٍ أدنى لاستخدام هذه الحزمة.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>If you are unsure, install the latest binaries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">وإذا لم تكن متأكدًا ، فثبت الملفات الثنائية الأخيرة.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>If you are upgrading from Microsoft Dynamics AX 2012, install the following application X++ fixes in the destination environment before you run the data upgrade:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">إذا كنت تقوم بالترقية من Microsoft Dynamics AX 2012، فثبّت الإصلاحات العاجلة X++ التالية للتطبيق في البيئة الوجهة قبل تشغيل ترقيه البيانات.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>KB 4033183 - Dynamics AX 2012 R2 or Dynamics AX 2012 R3 Pre-CU8 non-retail upgrade fails with Object not found for dbo.RETAILTILLLAYOUTZONE.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KB 4033183 - فشلت ترقية Dynamics AX 2012 R2 أو Dynamics AX 2012 R3 Pre-CU8 لا علاقة لها بالبيع بالتجزئة وعدم العثور على "كائن" لـ dbo.RETAILTILLLAYOUTZONE.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>KB 4040692 - Dynamics AX 2012 R3 to Microsoft Dynamics 365 for Operations 7.2 upgrade fails on RetailSalesLine duplicate index on SalesLineIdx.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KB 4040692 - فشلت ترقية AX 2012 R3 إلى Microsoft Dynamics 365 for Operations 7.2 على فهرس RetailSalesLine المكرر على SalesLineIdx.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>KB 4035490 - Performance issue with GeneralJournalAccountEntry MainAccount field upgrade script.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">KB 4035490 - مشكلة في الأداء مع البرنامج النصي لترقية الحقل GeneralJournalAccountEntry MainAccount.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Follow these steps to run the Environment reprovisioning tool.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">اتبع الخطوات التالية لتشغيل أداه إعادة تزويد البيئة.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In the Shared asset library, select <bpt id="p1">**</bpt>Software deployable package<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">في مكتبه الأصول المشتركة، حدد <bpt id="p1">**</bpt>حزمة قابلة للنشر للبرنامج‬<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Download the Environment reprovisioning tool.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">قم بتنزيل أداه إعادة تزويد البيئة.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>In the asset library for your project, select <bpt id="p1">**</bpt>Software deployable package<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">في مكتبه الأصول المشتركة لمشروعك، حدد <bpt id="p1">**</bpt>حزمة قابلة للنشر للبرنامج‬<ept id="p1">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Select <bpt id="p1">**</bpt>New<ept id="p1">**</ept> to create a new package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">حدد <bpt id="p1">**</bpt>جديد<ept id="p1">**</ept> لإنشاء حزمة جديدة.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Enter a name and description for the package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">أدخل اسمًا ووصفًا للحزمة.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>You can use <bpt id="p1">**</bpt>Environment reprovisioning tool<ept id="p1">**</ept> as the package name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">يمكنك استخدام <bpt id="p1">**</bpt>أداة إعادة تزويد البيئة<ept id="p1">**</ept> كاسم للحزمة.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Upload the package that you downloaded earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">حمّل الحزمة التي قمت بتنزيلها في وقت سابق.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>On the <bpt id="p1">**</bpt>Environment details<ept id="p1">**</ept> page for your target environment, select <bpt id="p2">**</bpt>Maintain<ept id="p2">**</ept><ph id="ph1"> &gt; </ph><bpt id="p3">**</bpt>Apply updates<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">في صفحة <bpt id="p1">**</bpt>تفاصيل البيئة<ept id="p1">**</ept> للبيئة الهدف، حدد <bpt id="p2">**</bpt>صيانة‏‎‏‎<ept id="p2">**</ept><ph id="ph1"> &gt; </ph><bpt id="p3">**</bpt>تطبيق التحديثات<ept id="p3">**</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Select the Environment reprovisioning tool that you uploaded earlier, and then select <bpt id="p1">**</bpt>Apply<ept id="p1">**</ept> to apply the package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">حدد أداه إعادة تزويد البيئة التي قمت بتحميلها في وقت سابق، ثم حدد <bpt id="p1">**</bpt>تطبيق<ept id="p1">**</ept> لتطبيق الحزمة.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Monitor the progress of the package deployment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">راقب تقدم نشر الحزمة.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>For more information about how to apply a deployable package, see <bpt id="p1">[</bpt>Apply a deployable package<ept id="p1">](../deployment/create-apply-deployable-package.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">لمزيد من المعلومات حول كيفية تطبيق حزمة قابلة للنشر، راجع <bpt id="p1">[</bpt>تطبيق حزمة قابلة للنشر<ept id="p1">](../deployment/create-apply-deployable-package.md)</ept>.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>For more information about how to manually apply a deployable package, see <bpt id="p1">[</bpt>Install a deployable package<ept id="p1">](../deployment/install-deployable-package.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">لمزيد من المعلومات حول كيفية تطبيق حزمة قابلة للنشر يدويًا، راجع <bpt id="p1">[</bpt>تثبيت حزمة قابلة للنشر<ept id="p1">](../deployment/install-deployable-package.md)</ept>.</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>