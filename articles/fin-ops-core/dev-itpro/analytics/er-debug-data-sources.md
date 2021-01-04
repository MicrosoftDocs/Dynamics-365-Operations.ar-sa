---
title: تصحيح مصادر البيانات لتنسيق ER الذي تم تنفيذه لتحليل تدفق البيانات وتحويلها
description: يشرح هذا الموضوع كيف يمكنك تصحيح مصادر البيانات لتنسيق ER الذي تم تنفيذه لفهم تدفق البيانات الذي تم تكوينه وتحويلها بشكل أفضل.
author: NickSelin
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 3a486800f37dda7829aeeaa56a30285a92a61b9d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680772"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a><span data-ttu-id="95f6a-103">تصحيح مصادر البيانات لتنسيق ER الذي تم تنفيذه لتحليل تدفق البيانات وتحويلها</span><span class="sxs-lookup"><span data-stu-id="95f6a-103">Debug data sources of an executed ER format to analyze data flow and transformation</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="95f6a-104">عندما تقوم [بتكوين](tasks/er-format-configuration-2016-11.md) حل التقارير الإلكترونية (ER) لإنشاء المستندات الصادرة، يمكنك تحديد الطرق المستخدمة للحصول على البيانات من التطبيق وإدخالها في الإخراج الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="95f6a-104">When you [configure](tasks/er-format-configuration-2016-11.md) an Electronic reporting (ER) solution to generate outbound documents, you define the methods that are used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="95f6a-105">لجعل دعم دوره الحياة لحل ER أكثر كفاءة، يجب أن يتكون الحل الخاص بك من [نموذج بيانات](general-electronic-reporting.md#DataModelComponent) التقارير الإلكترونية ومكونات [التعيين](general-electronic-reporting.md#ModelMappingComponent) الخاصة به، وكذلك [تنسيق](general-electronic-reporting.md#FormatComponentOutbound) التقارير الإلكترونية بحيث يكون تعيين النموذج خاص بالتطبيق، بينما تبقي المكونات الأخرى غير محددة التطبيق.</span><span class="sxs-lookup"><span data-stu-id="95f6a-105">To make the life cycle support of the ER solution more efficient, your solution should consist of an ER [data model](general-electronic-reporting.md#DataModelComponent) and its [mapping](general-electronic-reporting.md#ModelMappingComponent) components, and also an ER [format](general-electronic-reporting.md#FormatComponentOutbound) and its mapping components, so that the model mapping is application-specific, whereas other components remain application-agnostic.</span></span> <span data-ttu-id="95f6a-106">ولذلك، قد [تؤثر](general-electronic-reporting.md#FormatComponentOutbound) العديد من مكونات ER على عمليه إدخال البيانات في الإخراج الذي تم إنشاؤه.</span><span class="sxs-lookup"><span data-stu-id="95f6a-106">Therefore, several ER components might [affect](general-electronic-reporting.md#FormatComponentOutbound) the process of entering data in the generated output.</span></span>

<span data-ttu-id="95f6a-107">في بعض الأحيان، تبدو بيانات الإخراج التي تم إنشاؤها مختلفه عن نفس البيانات في قاعده بيانات التطبيق.</span><span class="sxs-lookup"><span data-stu-id="95f6a-107">Sometimes, the data of the generated output looks different than the same data in the application database.</span></span> <span data-ttu-id="95f6a-108">في هذه الحالات، ستحتاج إلى تحديد أي من مكونات ER مسؤول عن تحويل البيانات.</span><span class="sxs-lookup"><span data-stu-id="95f6a-108">In these cases, you will want to determine which ER component is responsible for the data transformation.</span></span> <span data-ttu-id="95f6a-109">تقلل ميزة مصحح أخطاء مصدر البيانات الخاصة لـ ER الوقت والتكلفة المضمنة في هذا الاستقصاء بشكل ملحوظ.</span><span class="sxs-lookup"><span data-stu-id="95f6a-109">The ER data source debugger feature significantly reduces the time and cost that are involved in this investigation.</span></span> <span data-ttu-id="95f6a-110">يمكنك مقاطعه تنفيذ تنسيق ER وفتح واجهه مصحح أخطاء مصدر البيانات.</span><span class="sxs-lookup"><span data-stu-id="95f6a-110">You can interrupt the execution of an ER format and open the data source debugger interface.</span></span> <span data-ttu-id="95f6a-111">هناك، يمكنك استعراض مصادر البيانات المتوفرة وتحديد مصدر بيانات فردي لتنفيذه.</span><span class="sxs-lookup"><span data-stu-id="95f6a-111">There, you can browse the available data sources and select an individual data source for execution.</span></span> <span data-ttu-id="95f6a-112">يقوم التنفيذ اليدوي هذا بمحاكاة تنفيذ مصدر البيانات أثناء التشغيل الحقيقي لتنسيق ER.</span><span class="sxs-lookup"><span data-stu-id="95f6a-112">This manual execution simulates the execution of the data source during the real run of an ER format.</span></span> <span data-ttu-id="95f6a-113">يتم تقديم النتيجة في الصفحة التي يمكنك من خلالها تحليل البيانات التي تم استلامها.</span><span class="sxs-lookup"><span data-stu-id="95f6a-113">The result is presented on a page where you can analyze the data that is received.</span></span>

<span data-ttu-id="95f6a-114">لتشغيل ميزه تصحيح أخطاء مصدر البيانات، قم بتعيين الخيار **تمكين تصحيح البيانات عند تشغيل التنسيق** إلى **نعم** في معلمات مستخدم ER.</span><span class="sxs-lookup"><span data-stu-id="95f6a-114">To turn on the data source debugging feature, set the **Enable data debugging at format run** option to **Yes** in the ER user parameters.</span></span> <span data-ttu-id="95f6a-115">ثم يمكنك بدء تشغيل تصحيح مصدر البيانات أثناء تشغيل تنسيق ER لإنشاء المستندات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="95f6a-115">You can then start data source debugging while you run an ER format to generate outbound documents.</span></span> <span data-ttu-id="95f6a-116">يمكنك أيضا استخدام خيار **بدء التصحيح** لبدء تصحيح مصدر البيانات لتنسيق ER الذي تم تكوينه في [مصمم عمليات ER](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span><span class="sxs-lookup"><span data-stu-id="95f6a-116">You can also use the **Start debugging** option to initiate data source debugging for an ER format that is configured in the [ER Operation designer](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document).</span></span>

<span data-ttu-id="95f6a-117">يوفر هذا الموضوع إرشادات لبدء تصحيح أخطاء مصدر البيانات لتنسيقات ER التي تم تنفيذها.</span><span class="sxs-lookup"><span data-stu-id="95f6a-117">This topic provides guidelines for initiating data source debugging for executed ER formats.</span></span> <span data-ttu-id="95f6a-118">ويوضح كيف تساعدك المعلومات علي فهم تدفق البيانات وتحويلات البيانات.</span><span class="sxs-lookup"><span data-stu-id="95f6a-118">It explains how the information can help you understand the data flow and data transformations.</span></span> <span data-ttu-id="95f6a-119">تستخدم الامثله الموجودة في هذا الموضوع العملية التجارية لمعالجه مدفوعات المورد.</span><span class="sxs-lookup"><span data-stu-id="95f6a-119">The examples in this topic use the business process for vendor payments processing.</span></span>

## <a name="limitations"></a><span data-ttu-id="95f6a-120">قيود</span><span class="sxs-lookup"><span data-stu-id="95f6a-120">Limitations</span></span>

<span data-ttu-id="95f6a-121">يمكن استخدام مصحح أخطاء مصدر البيانات للوصول إلى بيانات مصادر البيانات التي يتم استخدامها في تنسيقات ER التي يتم تشغيلها لإنشاء المستندات الصادرة.</span><span class="sxs-lookup"><span data-stu-id="95f6a-121">The data source debugger can be used to access the data of data sources that are used in ER formats that are run to generate outbound documents.</span></span> <span data-ttu-id="95f6a-122">ولا يمكن استخدامه لتصحيح مصادر البيانات الخاصة بتنسيقات ER التي تم تصميمها لتحليل المستندات الواردة.</span><span class="sxs-lookup"><span data-stu-id="95f6a-122">It can't be used to debug data sources of ER formats that are designed to parse inbound documents.</span></span>

<span data-ttu-id="95f6a-123">لا يمكن الوصول حاليا إلى الإعدادات التالية الخاصة بتنسيقات ER لتصحيح مصدر البيانات:</span><span class="sxs-lookup"><span data-stu-id="95f6a-123">The following settings of ER formats aren't currently accessible for data source debugging:</span></span>

- <span data-ttu-id="95f6a-124">عمليات تحويل التنسيق</span><span class="sxs-lookup"><span data-stu-id="95f6a-124">Format transformations</span></span>
- <span data-ttu-id="95f6a-125">قواعد التحقق من صحة التنسيق والتعيين</span><span class="sxs-lookup"><span data-stu-id="95f6a-125">Format and mapping validation rules</span></span>
- <span data-ttu-id="95f6a-126">تعبيرات التمكين</span><span class="sxs-lookup"><span data-stu-id="95f6a-126">Enabling expressions</span></span>
- <span data-ttu-id="95f6a-127">تفاصيل تجميع البيانات في الذاكرة</span><span class="sxs-lookup"><span data-stu-id="95f6a-127">Details of in-memory data collection</span></span>

## <a name="prerequisites"></a><span data-ttu-id="95f6a-128">المتطلبات الأساسية</span><span class="sxs-lookup"><span data-stu-id="95f6a-128">Prerequisites</span></span>

- <span data-ttu-id="95f6a-129">لإكمال الامثله الموجودة في هذا الموضوع، يجب ان يكون لديك حق الوصول إلى [الأدوار](../sysadmin/tasks/assign-users-security-roles.md)التالية:</span><span class="sxs-lookup"><span data-stu-id="95f6a-129">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="95f6a-130">مطور إعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="95f6a-130">Electronic reporting developer</span></span>
    - <span data-ttu-id="95f6a-131">مستشار وظيفي لإعداد التقارير الإلكتروني</span><span class="sxs-lookup"><span data-stu-id="95f6a-131">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="95f6a-132">مسؤول النظام</span><span class="sxs-lookup"><span data-stu-id="95f6a-132">System administrator</span></span>

- <span data-ttu-id="95f6a-133">يجب تعيين الشركة علي **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-133">The company must be set to **DEMF**.</span></span>

- <span data-ttu-id="95f6a-134">اتبع الخطوات الموجودة في [الملحق 1](#appendix1) لهذا الموضوع لتنزيل مكونات حل Microsoft ER المطلوبة لمعالجة مدفوعات المورد.</span><span class="sxs-lookup"><span data-stu-id="95f6a-134">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the Microsoft ER solution that are required to process vendor payments.</span></span>
- <span data-ttu-id="95f6a-135">اتبع الخطوات الموجودة في [الملحق 2](#appendix2) لهذا الموضوع لاعداد الحسابات الدائنة لمعالجه دفع المورد من خلال استخدام حل ER الذي ستقوم بتنزيله.</span><span class="sxs-lookup"><span data-stu-id="95f6a-135">Follow the steps in [Appendix 2](#appendix2) of this topic to prepare Accounts payable for vendor payment processing by using the ER solution that you will download.</span></span>

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a><span data-ttu-id="95f6a-136">معالجه دفع المورد للحصول علي ملف دفع</span><span class="sxs-lookup"><span data-stu-id="95f6a-136">Process a vendor payment to get a payment file</span></span>

1. <span data-ttu-id="95f6a-137">اتبع الخطوات الموجودة في [الملحق 3](#appendix3) لهذا الموضوع لمعالجه مدفوعات المورد.</span><span class="sxs-lookup"><span data-stu-id="95f6a-137">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>

    ![معالجه دفع المورد قيد التقدم](./media/er-data-debugger-process-payment.png)

2. <span data-ttu-id="95f6a-139">قم بتنزيل ملف zip المضغوط إلى الكمبيوتر المحلي وقم بحفظه.</span><span class="sxs-lookup"><span data-stu-id="95f6a-139">Download and save the zip file to your local computer.</span></span>
3. <span data-ttu-id="95f6a-140">استخرج ملف دفع **ISO20022 Credit transfer.xml** من ملف zip.</span><span class="sxs-lookup"><span data-stu-id="95f6a-140">Extract the **ISO20022 Credit transfer.xml** payment file from the zip file.</span></span>
4. <span data-ttu-id="95f6a-141">قم بفتح ملف الدفع الذي تم استخراجه باستخدام عارض ملفات XML.</span><span class="sxs-lookup"><span data-stu-id="95f6a-141">Open the extracted payment file by using the XML file viewer.</span></span>

    <span data-ttu-id="95f6a-142">في ملف الدفع، لا يحتوي كود رقم الحساب البنكي الدولي (IBAN) الخاص بالحساب البنكي للمورد علي مسافات.</span><span class="sxs-lookup"><span data-stu-id="95f6a-142">In the payment file, the International Bank Account Number (IBAN) code of the vendor bank account contains no spaces.</span></span> <span data-ttu-id="95f6a-143">ولذلك فهو يختلف عن القيمة التي تم [إدخالها](#enteredIBANcode) في صفحة **الحسابات البنكية**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-143">Therefore, it differs from the value that was [entered](#enteredIBANcode) on the **Bank accounts** page.</span></span>

    ![رمز IBAN بدون مسافات](./media/er-data-debugger-payment-file.png)

    <span data-ttu-id="95f6a-145">يمكنك استخدام مصحح أخطاء مصدر بيانات ER لمعرفه أي من مكونات حل ER يتم استخدامه لاقتطاع المسافات في رمز IBAN.</span><span class="sxs-lookup"><span data-stu-id="95f6a-145">You can use the ER data source debugger to learn which component of the ER solution is used to truncate spaces in the IBAN code.</span></span>

## <a name="turn-on-data-source-debugging"></a><span data-ttu-id="95f6a-146">تشغيل تصحيح مصدر البيانات</span><span class="sxs-lookup"><span data-stu-id="95f6a-146">Turn on data source debugging</span></span>

1. <span data-ttu-id="95f6a-147">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-147">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="95f6a-148">في صفحة **التكوينات**، في جزء الإجراءات، في علامة التبويب **التكوينات**، في مجموعة **الإعدادات المتقدمة**، حدد **معلمات المستخدمين**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-148">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="95f6a-149">قم بتعيين الخيار **تمكين تصحيح البيانات عند تشغيل التنسيق** على القيمة **نعم**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-149">Set the **Enable data debugging at format run** option to **Yes**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="95f6a-150">هذه المعلمة خاصة بالمستخدم والشركة.</span><span class="sxs-lookup"><span data-stu-id="95f6a-150">This parameter is user-specific and company-specific.</span></span>

    ![مربع علامة تبويب معلمات المستخدمين](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a><span data-ttu-id="95f6a-152">معالجة دفع المورد لتصحيح الأخطاء</span><span class="sxs-lookup"><span data-stu-id="95f6a-152">Process a vendor payment for debugging</span></span>

1. <span data-ttu-id="95f6a-153">اتبع الخطوات الموجودة في [الملحق 3](#appendix3) لهذا الموضوع لمعالجه مدفوعات المورد.</span><span class="sxs-lookup"><span data-stu-id="95f6a-153">Follow the steps in [Appendix 3](#appendix3) of this topic to process vendor payments.</span></span>
2. <span data-ttu-id="95f6a-154">في مربع الرسالة، حدد **نعم** لتاكيد أنك تريد مقاطعة معالجه مدفوعات المورد وتبديل تصحيح مصدر البيانات على صفحة **تصحيح مصادر البيانات**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-154">In the message box, select **Yes** to confirm that you want to interrupt vendor payment processing and instead start data source debugging on the **Debug Datasources** page.</span></span>

    ![مربع رسالة التأكيد](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a><span data-ttu-id="95f6a-156">تصحيح مصادر البيانات المستخدمة في معالجه الدفع</span><span class="sxs-lookup"><span data-stu-id="95f6a-156">Debug data sources that are used in payment processing</span></span>

### <a name="debug-the-model-mapping"></a><span data-ttu-id="95f6a-157">تصحيح تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="95f6a-157">Debug the model mapping</span></span>

1. <span data-ttu-id="95f6a-158">في صفحة **تصحيح مصادر البيانات** ، في جزء الإجراءاتء، حدد **تعيين النموذج** لبدء التصحيح من مكون ER هذا.</span><span class="sxs-lookup"><span data-stu-id="95f6a-158">On the **Debug Datasources** page, on the Action Pane, select **Model mapping** to start to debug from this ER component.</span></span>
2. <span data-ttu-id="95f6a-159">في جزء مصدر البيانات الموجود علي اليمين، حدد مصدر البينات **notSentTransactions\$** ثم حدد **قراءه كافة السجلات**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-159">In the data source pane on the left, select the **\$notSentTransactions** data source, and then select **Read all records**.</span></span>

    <span data-ttu-id="95f6a-160">يمكنك تحديد **قراءة سجل 1**، أو **قراءه 10 سجلات** ، أو **قراءه 100 سجل**، أو **قراءه كافة السجلات** لفرض قراءة العدد المناسب للسجلات من مصدر البيانات المحدد.</span><span class="sxs-lookup"><span data-stu-id="95f6a-160">You can select **Read 1 record**, **Read 10 records**, **Read 100 records**, or **Read all records** to force the appropriate number of records to be read from the selected data source.</span></span> <span data-ttu-id="95f6a-161">وبهذه الطريقة، يمكنك محاكاة الوصول إلى مصدر البيانات من تنسيق ER الجاري تشغيله.</span><span class="sxs-lookup"><span data-stu-id="95f6a-161">In this way, you can simulate access to the data source from the running ER format.</span></span>

3. <span data-ttu-id="95f6a-162">في جزء البيانات على اليمين، حدد **توسيع الكل**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-162">In the data pane on the right, select **Expand all**.</span></span>

    <span data-ttu-id="95f6a-163">يمكنك رؤية ان مصدر البيانات المحدد من النوع **قائمة السجلات** يحتوي على سجل مفرد.</span><span class="sxs-lookup"><span data-stu-id="95f6a-163">You can see that the selected data source of the **Record list** type contains a single record.</span></span>

4. <span data-ttu-id="95f6a-164">قم بتوسيع مصدر بيانات **notSentTransactions\$** ، ثم حدد الأسلوب **vendBankAccountInTransactionCompany()**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-164">Expand the **\$notSentTransactions** data source, and select the nested **vendBankAccountInTransactionCompany()** method.</span></span>
5. <span data-ttu-id="95f6a-165">قم بتوسيع أسلوب **vendBankAccountInTransactionCompany()** ، ثم حدد حقل **IBAN** المتداخل.</span><span class="sxs-lookup"><span data-stu-id="95f6a-165">Expand the **vendBankAccountInTransactionCompany()** method, and select the nested **IBAN** field.</span></span>
6. <span data-ttu-id="95f6a-166">حدد **الحصول على قيمة**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-166">Select **Get value**.</span></span>

    <span data-ttu-id="95f6a-167">يمكنك تحديد **الحصول على قيمة** لفرض قيمة حقل محدد لمصدر البيانات المحدد لتتم قراءته.</span><span class="sxs-lookup"><span data-stu-id="95f6a-167">You can select **Get value** to force the value of a selected field of the selected data source to be read.</span></span> <span data-ttu-id="95f6a-168">وبهذه الطريقة، يمكنك محاكاة الوصول إلى هذا الحقل من تنسيق ER الجاري تشغيله.</span><span class="sxs-lookup"><span data-stu-id="95f6a-168">In this way, you can simulate access to this field from the running ER format.</span></span>

7. <span data-ttu-id="95f6a-169">حدد **توسيع الكل‬**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-169">Select **Expand all**.</span></span>

    ![قيمه حقل IBAN في تعيين النموذج](./media/er-data-debugger-debugging-model-mapping.png)

    <span data-ttu-id="95f6a-171">وكما تري، تعيين النموذج غير مسؤول عن المساحات المقتطعة، لأن رمز IBAN الذي يرجع للحساب البنكي للمورد يتضمن مسافات.</span><span class="sxs-lookup"><span data-stu-id="95f6a-171">As you can see, the model mapping isn't responsible for the truncated spaces, because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="95f6a-172">ولذلك، يجب متابعه تصحيح مصدر البيانات.</span><span class="sxs-lookup"><span data-stu-id="95f6a-172">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format-mapping"></a><span data-ttu-id="95f6a-173">تصحيح تعيين التنسيق</span><span class="sxs-lookup"><span data-stu-id="95f6a-173">Debug the format mapping</span></span>

1. <span data-ttu-id="95f6a-174">في صفحة **تصحيح مصادر البيانات** ، في جزء الإجراءاتء، حدد **تعيين التنسيق** لبدء التصحيح من مكون ER هذا.</span><span class="sxs-lookup"><span data-stu-id="95f6a-174">On the **Debug Datasources** page, on the Action Pane, select **Format mapping** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="95f6a-175">حدد مصدر بيانات **\$PaymentByDebtor‎** ، ثم حدد **قراءة كافة السجلات**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-175">Select the **\$PaymentByDebtor** data source, and then select **Read all records**.</span></span>
3. <span data-ttu-id="95f6a-176">قم بتوسيع **\$PaymentByDebtor**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-176">Expand **\$PaymentByDebtor**.</span></span>
4. <span data-ttu-id="95f6a-177">قم بتوسيع **\$PaymentByDebtor.Lines** ، ثم حدد **قراءة كافة السجلات**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-177">Expand **\$PaymentByDebtor.Lines**, and then select **Read all records**.</span></span>
5. <span data-ttu-id="95f6a-178">قم بتوسيع **\$PaymentByDebtor.Lines.CreditorAccount**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-178">Expand **\$PaymentByDebtor.Lines.CreditorAccount**.</span></span>
6. <span data-ttu-id="95f6a-179">قم بتوسيع **\$PaymentByDebtor.Lines.CreditorAccount.Identification** ثم حدد **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-179">Expand **\$PaymentByDebtor.Lines.CreditorAccount.Identification**, and then select **\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN**.</span></span>
7. <span data-ttu-id="95f6a-180">حدد **الحصول على قيمة**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-180">Select **Get value**.</span></span>
8. <span data-ttu-id="95f6a-181">حدد **توسيع الكل‬**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-181">Select **Expand all**.</span></span>

    ![قيمه حقل IBAN في تعيين التنسيق](./media/er-data-debugger-debugging-format-mapping.png)

    <span data-ttu-id="95f6a-183">وكما تري، مصادر البيانات لتعيين التنسيق غير مسؤولة عن المساحات المقتطعة، لأن رمز IBAN الذي يرجع للحساب البنكي للمورد يتضمن مسافات.</span><span class="sxs-lookup"><span data-stu-id="95f6a-183">As you can see, the data sources of the format mapping aren't responsible for the truncated spaces, because the IBAN code that they return for the vendor bank account includes spaces.</span></span> <span data-ttu-id="95f6a-184">ولذلك، يجب متابعه تصحيح مصدر البيانات.</span><span class="sxs-lookup"><span data-stu-id="95f6a-184">Therefore, you must continue data source debugging.</span></span>

### <a name="debug-the-format"></a><span data-ttu-id="95f6a-185">تصحيح التنسيق</span><span class="sxs-lookup"><span data-stu-id="95f6a-185">Debug the format</span></span>

1. <span data-ttu-id="95f6a-186">في صفحة **تصحيح مصادر البيانات** ، في جزء الإجراءاتء، حدد **التنسيق** لبدء التصحيح من مكون ER هذا.</span><span class="sxs-lookup"><span data-stu-id="95f6a-186">On the **Debug Datasources** page, on the Action Pane, select **Format** to continue to debug from this ER component.</span></span>
2. <span data-ttu-id="95f6a-187">قم بتوسيع عناصر التنسيق لتحديد **ISO20022CTReports** \> **XMLHeader** \> **مستند** \> **CstmrCdtTrfInitn** \> **PmtInf** ثم حدد **قراءة كافة السجلات**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-187">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf**, and then select **Read all records**.</span></span>
3. <span data-ttu-id="95f6a-188">قم بتوسيع عناصر التنسيق لتحديد **ISO20022CTReports** \> **XMLHeader** \> **مستند** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**، ثم حدد **قراءة كافة السجلات**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-188">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf**, and then select **Read all records**.</span></span>
4. <span data-ttu-id="95f6a-189">قم بتوسيع عناصر التنسيق لتحديد **ISO20022CTReports** \> **XMLHeader** \> **مستند** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **معرّف** \> **IBAN** \> **BankIBAN** ثم حدد **الحصول على قيمة**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-189">Expand the format elements to select **ISO20022CTReports** \> **XMLHeader** \> **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**, and then select **Get value**.</span></span>
5. <span data-ttu-id="95f6a-190">حدد **توسيع الكل‬**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-190">Select **Expand all**.</span></span>

    ![قيمه حقل IBAN في التنسيق](./media/er-data-debugger-debugging-format.png)

   <span data-ttu-id="95f6a-192">وكما تري، رابط التنسيق غير مسؤول عن المساحات المقتطعة، لأن رمز IBAN الذي يرجع للحساب البنكي للمورد يتضمن مسافات.</span><span class="sxs-lookup"><span data-stu-id="95f6a-192">As you can see, the format binding isn't responsible for the truncated spaces because the IBAN code that it returns for the vendor bank account includes spaces.</span></span> <span data-ttu-id="95f6a-193">لذلك، يتم تكوين عنصر **BankIBAN** لاستخدام تحويل التنسيق الذي يقوم باقتطاع المساحات.</span><span class="sxs-lookup"><span data-stu-id="95f6a-193">Therefore, the **BankIBAN** element is configured to use a format transformation that truncates spaces.</span></span>

6. <span data-ttu-id="95f6a-194">أغلق مصحح أخطاء مصدر البيانات.</span><span class="sxs-lookup"><span data-stu-id="95f6a-194">Close the data source debugger.</span></span>

### <a name="review-the-format-transformations"></a><span data-ttu-id="95f6a-195">مراجعة عمليات تحويل التنسيق</span><span class="sxs-lookup"><span data-stu-id="95f6a-195">Review the format transformations</span></span>

1. <span data-ttu-id="95f6a-196">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-196">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="95f6a-197">في صفحة **التكوينات** حدد **نموذج الدفع** \> **تحويل ائتمان ISO20022**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-197">On the **Configurations** page, select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="95f6a-198">حدد **المصمم** ثم قم بتوسيع العناصر لتحديد **مستند** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **معرف** \> **IBAN** \> **BankIBAN**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-198">Select **Designer**, and then expand the elements to select **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN**.</span></span>

    ![عنصر BankIBAN في صفحة مصمم التنسيق](./media/er-data-debugger-referred-transformation.png)

    <span data-ttu-id="95f6a-200">وكما تري، يتم تكوين عنصر **BankIBAN** لاستخدام التحويل **استثناء الأبجدي الرقمي من الإزالة**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-200">As you can see, the **BankIBAN** element is configured to use the **remove not alphanumeric** transformation.</span></span>

4. <span data-ttu-id="95f6a-201">حدد علامة تبويب **عمليات التحويل**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-201">Select the **Transformations** tab.</span></span>

    ![علامة تبويب عمليات التحويل لعنصر BankIBAN](./media/er-data-debugger-transformation.png)

    <span data-ttu-id="95f6a-203">وكما تري، يتم تكوين تحويل **استثناء الأبجدي الرقي من الإزالة** لاستخدام تعبير يقوم باقتطاع المسافات من السلسلة النصية المتوفرة.</span><span class="sxs-lookup"><span data-stu-id="95f6a-203">As you can see, the **remove not alphanumeric** transformation is configured to use an expression that truncates spaces from the text string that is provided.</span></span>

## <a name="start-to-debug-in-the-operation-designer"></a><span data-ttu-id="95f6a-204">البدء في التصحيح في مصمم العملية</span><span class="sxs-lookup"><span data-stu-id="95f6a-204">Start to debug in the Operation designer</span></span>

<span data-ttu-id="95f6a-205">عند تكوين إصدار مسودة من تنسيق ER الذي يمكن تشغيله مباشره من "مصمم العملية"، يمكنك الوصول إلى مصحح أخطاء مصدر البيانات عن طريق تحديد **بدء التصحيح** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="95f6a-205">When you configure a draft version of the ER format that can be run directly from the Operation designer, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![زر بدء التصحيح في صفحة مصمم التنسيق](./media/er-data-debugger-run-from-designer.png)

<span data-ttu-id="95f6a-207">تتوفر مكونات تعيين التنسيق والتنسيق لتنسيق ER الذي يتم تحريره للتصحيح.</span><span class="sxs-lookup"><span data-stu-id="95f6a-207">The format mapping and format components of the ER format that is being edited are available for debugging.</span></span>

## <a name="start-to-debug-in-the-model-mapping-designer"></a><span data-ttu-id="95f6a-208">البدء في التصحيح في مصمم تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="95f6a-208">Start to debug in the Model mapping designer</span></span>

<span data-ttu-id="95f6a-209">عند تكوين تعيين نموذج ER الذي يمكن تشغيله من صفحة **تعيين النموذج** يمكنك الوصول إلى مصحح أخطاء مصدر البيانات عن طريق تحديد **بدء التصحيح** في جزء الإجراءات.</span><span class="sxs-lookup"><span data-stu-id="95f6a-209">When you configure an ER model mapping that can be run from the **Model mapping** page, you can access the data source debugger by selecting **Start Debugging** on the Action Pane.</span></span>

![زر بدء التصحيح في صفحة مصمم تعيين النموذج](./media/er-data-debugger-run-from-designer-mapping.png)

<span data-ttu-id="95f6a-211">يتوفر مكون تعيين النموذج لتعيين ER الجاري تحريره للتصحيح.</span><span class="sxs-lookup"><span data-stu-id="95f6a-211">The model mapping component of the ER mapping that is being edited is available for debugging.</span></span>

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a><span data-ttu-id="95f6a-212">الملحق 1: الحصول على حل ER</span><span class="sxs-lookup"><span data-stu-id="95f6a-212">Appendix 1: Get an ER solution</span></span>

### <a name="download-an-er-solution"></a><span data-ttu-id="95f6a-213">تنزيل حل تقارير إلكترونية</span><span class="sxs-lookup"><span data-stu-id="95f6a-213">Download an ER solution</span></span>

<span data-ttu-id="95f6a-214">إذا كنت ترغب في استخدام حل ER لإنشاء ملف دفع إلكتروني لدفع المورد الذي تتم معالجته، فانه يمكنك [تنزيل](download-electronic-reporting-configuration-lcs.md) تنسيق دفع ER لـ **تحويل ائتمان ISO20022** المتوفر من مكتبه الأصول المشتركة في Microsoft Dynamics Lifecycle Services أو من المستودع العمومي.</span><span class="sxs-lookup"><span data-stu-id="95f6a-214">If you want to use an ER solution to generate an electronic payment file for a vendor payment that is processed, you can [download](download-electronic-reporting-configuration-lcs.md) the **ISO20022 Credit transfer** ER payment format that is available from the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) or from the Global repository.</span></span>

![استيراد تنسيق دفع ER على صفحة مستودع التكوين](./media/er-data-debugger-import-from-repo.png)

<span data-ttu-id="95f6a-216">بالاضافه إلى التنسيق ER المحدد، يجب استيراد [التكوينات](general-electronic-reporting.md#Configuration) التالية تلقائيًا في مثيل Microsoft Dynamics 365 Finance كجزء من حل ER لـ **تحويل ائتمان ISO20022**:</span><span class="sxs-lookup"><span data-stu-id="95f6a-216">In addition to the selected ER format, the following [configurations](general-electronic-reporting.md#Configuration) must be automatically imported into your Microsoft Dynamics 365 Finance instance as part of the **ISO20022 Credit transfer** ER solution:</span></span>

- <span data-ttu-id="95f6a-217">**نموذج الدفع** [تكوين نموذج بيانات ER](general-electronic-reporting.md#DataModelComponent)</span><span class="sxs-lookup"><span data-stu-id="95f6a-217">**Payment model** [ER data model configuration](general-electronic-reporting.md#DataModelComponent)</span></span>
- <span data-ttu-id="95f6a-218">**تحويل الائتمان ISO20022** [تكوين تنسيق ER](general-electronic-reporting.md#FormatComponentOutbound)</span><span class="sxs-lookup"><span data-stu-id="95f6a-218">**ISO20022 Credit transfer** [ER format configuration](general-electronic-reporting.md#FormatComponentOutbound)</span></span>
- <span data-ttu-id="95f6a-219">**تعيين نموذج الدفع 1611** [تكوين تعيين نموذج ER](general-electronic-reporting.md#ModelMappingComponent)</span><span class="sxs-lookup"><span data-stu-id="95f6a-219">**Payment model mapping 1611** [ER model mapping configuration](general-electronic-reporting.md#ModelMappingComponent)</span></span>
- <span data-ttu-id="95f6a-220">**تعيين نموذج الدفع للوجهة ISO20022** تكوين تعيين نموذج ER</span><span class="sxs-lookup"><span data-stu-id="95f6a-220">**Payment model mapping to destination ISO20022** ER model mapping configuration</span></span>

<span data-ttu-id="95f6a-221">يمكنك العثور علي هذه التكوينات في صفحة **التكوينات** الخاصة بإطار عمل ER (**إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**).</span><span class="sxs-lookup"><span data-stu-id="95f6a-221">You can find these configurations on the **Configurations** page of the ER framework (**Organization administration** \> **Electronic reporting** \> **Configurations**).</span></span>

![التكوينات المستوردة على صفحة التكوينات](./media/er-data-debugger-configurations.png)

<span data-ttu-id="95f6a-223">إذا كان أي من التكوينات التي تم سردها سابقًا مفقودا في شجرة التكوين، فيجب تنزيلها يدويا من مكتبه الأصول المشتركة LCS بنفس الطريقة التي قمت بها بتنزيل تنسيق دفع **تحويل ائتمان ISO20022**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-223">If any of the previously listed configurations are missing in the configuration tree, you must manually download them from the LCS Shared asset library in the same way that you downloaded the **ISO20022 Credit transfer** ER payment format.</span></span>

### <a name="analyze-the-downloaded-er-solution"></a><span data-ttu-id="95f6a-224">تحليل حل ER الذي تم تنزيله</span><span class="sxs-lookup"><span data-stu-id="95f6a-224">Analyze the downloaded ER solution</span></span>

#### <a name="review-the-model-mapping"></a><span data-ttu-id="95f6a-225">مراجعة تعيين النموذج</span><span class="sxs-lookup"><span data-stu-id="95f6a-225">Review the model mapping</span></span>

1. <span data-ttu-id="95f6a-226">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-226">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="95f6a-227">حدد **نموذج الدفع** \> **تعيين نموذج دفع 1611**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-227">Select **Payment model** \> **Payment model mapping 1611**.</span></span>
3. <span data-ttu-id="95f6a-228">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-228">Select **Designer**.</span></span>
4. <span data-ttu-id="95f6a-229">حدد سجل تعيين **تعيين نموذج الدفع ISO20022 CT**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-229">Select the **Payment model mapping ISO20022 CT** mapping record.</span></span>
5. <span data-ttu-id="95f6a-230">قم بتحديد **المصصم**، ثم قم بمراجعه تعيين النموذج المفتوح.</span><span class="sxs-lookup"><span data-stu-id="95f6a-230">Select **Designer**, and then review the model mapping that is opened.</span></span>

    <span data-ttu-id="95f6a-231">لاحظ أن حقل **المدفوعات** لنموذج البيانات مرتبط بمصدر بيانات **\$notSentTransactions‎** الذي يقوم بإرجاع قائمه بنود دفع المورد التي تتم معالجتها.</span><span class="sxs-lookup"><span data-stu-id="95f6a-231">Notice that the **Payments** field of the data model is bound to the **\$notSentTransactions** data source that returns the list of vendor payment lines that are being processed.</span></span>

    ![حقل المدفوعات في صفحة مصمم تعيين النموذج](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a><span data-ttu-id="95f6a-233">مراجعة تعيين التنسيق</span><span class="sxs-lookup"><span data-stu-id="95f6a-233">Review the format mapping</span></span>

1. <span data-ttu-id="95f6a-234">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-234">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="95f6a-235">حدد **نموذج الدفع** \> **تحويل ائتمان ISO20022**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-235">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="95f6a-236">حدد **المصمم**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-236">Select **Designer**.</span></span>
4. <span data-ttu-id="95f6a-237">في علامة التبويب **التعيين** راجع تعيين التنسيق الذي سيتم فتحه.</span><span class="sxs-lookup"><span data-stu-id="95f6a-237">On the **Mapping** tab, review the format mapping that is opened.</span></span>

    <span data-ttu-id="95f6a-238">لاحظ أن عنصر **مستند** \> **CstmrCdtTrfInitn** \> **PmtInf** للملف **ISO20022CTReports** \> **XMLHeader** مرتبط بمصدر بيانات **\$PaymentByDebtor** المكوّن على سجلات مجموعة حقل **المدفوعات** لنموذج البينات.</span><span class="sxs-lookup"><span data-stu-id="95f6a-238">Notice that the **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** element of the **ISO20022CTReports** \> **XMLHeader** file is bound to the **\$PaymentByDebtor** data source that is configured to group records of the data model's **Payments** field.</span></span>

    ![عنصر PmtInf في صفحة مصمم التنسيق](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a><span data-ttu-id="95f6a-240">مراجعة التنسيق</span><span class="sxs-lookup"><span data-stu-id="95f6a-240">Review the format</span></span>

1. <span data-ttu-id="95f6a-241">انتقل إلى **إدارة المؤسسة** \> **التقارير الإلكترونية** \> **التكوينات**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-241">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="95f6a-242">حدد **نموذج الدفع** \> **تحويل ائتمان ISO20022**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-242">Select **Payment model** \> **ISO20022 Credit transfer**.</span></span>
3. <span data-ttu-id="95f6a-243">قم بتحديد **المصصم**، ثم قم بمراجعه التنسيق المفتوح.</span><span class="sxs-lookup"><span data-stu-id="95f6a-243">Select **Designer**, and then review the format that is opened.</span></span>

    <span data-ttu-id="95f6a-244">لاحظ أن عنصر التنسيق ضمن **مستند** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **معرف** \> **IBAN** \> **BankIBAN** مكوّن لإدخال رمز IBAN لحساب المورد في ملف الدفع.</span><span class="sxs-lookup"><span data-stu-id="95f6a-244">Notice that the format element under **Document** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** is configured to enter the IBAN code of the vendor account in the payment file.</span></span>

    ![عنصر BankIBAN في صفحة مصمم التنسيق](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a><span data-ttu-id="95f6a-246">ملحق 2: تكوين الحسابات الدائنة</span><span class="sxs-lookup"><span data-stu-id="95f6a-246">Appendix 2: Configure Accounts payable</span></span>

### <a name="modify-a-vendor-property"></a><span data-ttu-id="95f6a-247">تعديل خاصية مورد</span><span class="sxs-lookup"><span data-stu-id="95f6a-247">Modify a vendor property</span></span>

1. <span data-ttu-id="95f6a-248">انتقل إلى **الحسابات الدائنة** \> **الموردون** \> **كافة الموردين**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-248">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="95f6a-249">حدد المورد **DE-01002** ، ثم، في جزء الإجراءات، في علامة تبويب **المورد** في مجموعة **الإعداد** حدد **الحسابات البنكية**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-249">Select vendor **DE-01002**, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="95f6a-250">في علامة التبويب السريعة **الهوية** ، في حقل **IBAN** ، <a name="enteredIBANcode"></a>أدخل **GB33 BUKB 2020 1555 5555 55**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-250">On the **Identification** FastTab, in the **IBAN** field, <a name="enteredIBANcode"></a>enter **GB33 BUKB 2020 1555 5555 55**.</span></span>
4. <span data-ttu-id="95f6a-251">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-251">Select **Save**.</span></span>

![تعيين حقل IBAN في صفحة الحسابات البنكية للمورد](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a><span data-ttu-id="95f6a-253">إعداد طريقة الدفع</span><span class="sxs-lookup"><span data-stu-id="95f6a-253">Set up a method of payment</span></span>

1. <span data-ttu-id="95f6a-254">انتقل إلى **الحسابات الدائنة** \> **إعداد الدفع** \> **طرق الدفع**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-254">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="95f6a-255">حدد طريقة الدفع **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-255">Select the **SEPA CT** payment method.</span></span>
3. <span data-ttu-id="95f6a-256">في علامة التبويب السريعة **تنسيقات الملف** في قسم **تنسيقات الملف** قم بتعيين خيار **تنسيق التصدير الإلكتروني العام**‬ على **نعم**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-256">On the **File formats** FastTab, in the **File formats** section, set the **Generic electronic Export format** option to **Yes**.</span></span>
4. <span data-ttu-id="95f6a-257">في حقل **تكوين تنسيق التصدير** ، حدد تنسيق ER لـ **تحويل ائتمان ISO20022**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-257">In the **Export format configuration** field, select the **ISO20022 Credit transfer** ER format.</span></span>
5. <span data-ttu-id="95f6a-258">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-258">Select **Save**.</span></span>

![إعدادات تنسيق الملف في صفحة طرق الدفع](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a><span data-ttu-id="95f6a-260">إضافة دفعة مورد​</span><span class="sxs-lookup"><span data-stu-id="95f6a-260">Add a vendor payment</span></span>

1. <span data-ttu-id="95f6a-261">انتقل إلى **الحسابات الدائنة** \> **المدفوعات** \> **‏‫دفتر يومية المدفوعات للمورد‬**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-261">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="95f6a-262">إضافة دفتر يومية مدفوعات جديد.</span><span class="sxs-lookup"><span data-stu-id="95f6a-262">Add a new payment journal.</span></span>
3. <span data-ttu-id="95f6a-263">حدد **البنود** وقم بإضافة بند دفع جديد.</span><span class="sxs-lookup"><span data-stu-id="95f6a-263">Select **Lines**, and add a new payment line.</span></span>
4. <span data-ttu-id="95f6a-264">في حقل **الحساب** حدد المورد **DE-01002**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-264">In the **Account** field, select vendor **DE-01002**.</span></span>
5. <span data-ttu-id="95f6a-265">في الحقل **مدين** ، أدخل قيمة.</span><span class="sxs-lookup"><span data-stu-id="95f6a-265">In the **Debit** field, enter a value.</span></span>
6. <span data-ttu-id="95f6a-266">في حقل **طريقة الدفع** حدد **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-266">In the **Method of payment** field, select **SEPA CT**.</span></span>
7. <span data-ttu-id="95f6a-267">حدد **حفظ**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-267">Select **Save**.</span></span>

![إضافة دفع المورد في صفحة مدفوعات المورد](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a><span data-ttu-id="95f6a-269">ملحق 3: معالجة دفع المورد</span><span class="sxs-lookup"><span data-stu-id="95f6a-269">Appendix 3: Process a vendor payment</span></span>

1. <span data-ttu-id="95f6a-270">انتقل إلى **الحسابات الدائنة** \> **المدفوعات** \> **‏‫دفتر يومية المدفوعات للمورد‬**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-270">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="95f6a-271">في صفحة **‏‫دفتر يومية المدفوعات للمورد‬** ، حدد دفتر يوميه المدفوعات الذي قمت بإنشاءه مسبقا، ثم حدد **البنود**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-271">On the **Vendor payment journal** page, select the payment journal that you previously created, and then select **Lines**.</span></span>
3. <span data-ttu-id="95f6a-272">حدد بند الدفع، ثم قم بتحديد **حالة الدفع** \> **بلا**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-272">Select the payment line, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="95f6a-273">حدد **إنشاء المدفوعات**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-273">Select **Generate payments**.</span></span>
5. <span data-ttu-id="95f6a-274">في حقل **طريقة الدفع** حدد **SEPA CT**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-274">In the **Method of payment** field, select **SEPA CT**.</span></span>
6. <span data-ttu-id="95f6a-275">في الحقل **حساب البنك** حدد **DEMF OPER**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-275">In the **Bank account** field, select **DEMF OPER**.</span></span>
7. <span data-ttu-id="95f6a-276">في مربع الحوار **إنشاء المدفوعات‬‏‫** حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-276">In the **Generate payments** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="95f6a-277">في مربع الحوار **معلمات التقارير الإلكترونية** حدد **موافق**.</span><span class="sxs-lookup"><span data-stu-id="95f6a-277">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
