---
title: "تكوين تكامل كشف المرتبات بين Talent وDayforce"
description: "يشرح هذا الموضوع كيفية تكوين التكامل بين Microsoft Dynamics 365 for Talent وCeridian Dayforce لكي تتمكن من معالجة دورة دفع."
author: jcart1106
manager: AnnBe
ms.date: 07/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: fcddf82cffb9f0ba94b83eb21809b810585ebc9e
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---

# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="70f1f-103">تكوين تكامل كشف المرتبات بين Talent وDayforce</span><span class="sxs-lookup"><span data-stu-id="70f1f-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="70f1f-104">يعتمد التكامل بين Microsoft Dynamics 365 for Talent وCeridian Dayforce على العديد من خطوات التكوين التي تم وصفها في هذا الموضوع.</span><span class="sxs-lookup"><span data-stu-id="70f1f-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="70f1f-105">يجب عليك تكوين التكامل في كل من Talent وDayforce قبل أن تتمكن من معالجة دورة دفع.</span><span class="sxs-lookup"><span data-stu-id="70f1f-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="70f1f-106">عندما تستخدم خدمة مثل Dayforce لإتمام دورات الدفع، يجب عليك تمكين التكامل في Talent.</span><span class="sxs-lookup"><span data-stu-id="70f1f-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="70f1f-107">يتطلب التكامل بيانات معينة من Talent.</span><span class="sxs-lookup"><span data-stu-id="70f1f-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="70f1f-108">لذلك، يجب عليك التأكد من أن البيانات التي تم تعيينها إلى Dayforce هي بيانات تم تكوينها في Talent بطريقة تدعم التكامل.</span><span class="sxs-lookup"><span data-stu-id="70f1f-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="70f1f-109">يستخدم التكامل الفئات الواسعة التالية من البيانات:</span><span class="sxs-lookup"><span data-stu-id="70f1f-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="70f1f-110">بيانات الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="70f1f-110">Human resources data</span></span>
- <span data-ttu-id="70f1f-111">بيانات التعويض</span><span class="sxs-lookup"><span data-stu-id="70f1f-111">Compensation data</span></span>
- <span data-ttu-id="70f1f-112">بيانات كشف المرتبات، مثل دورات الدفع وفترات الدفع وأكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="70f1f-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="70f1f-113">بيانات العامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-113">Worker data</span></span>

<span data-ttu-id="70f1f-114">يصف هذا الموضوع الخطوات التي يجب اتباعها لتمكين التكامل.</span><span class="sxs-lookup"><span data-stu-id="70f1f-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="70f1f-115">ويشرح أيضًا أنواع البيانات وتفاصيل التكوين التي يحتاج إليها التكامل.</span><span class="sxs-lookup"><span data-stu-id="70f1f-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="70f1f-116">تمكين التكامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-116">Enable the integration</span></span>

<span data-ttu-id="70f1f-117">في Talent، يجب تشغيل التكامل وإدخال معلومات التكوين للاتصال بخدمة Dayforce.</span><span class="sxs-lookup"><span data-stu-id="70f1f-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="70f1f-118">إذا أردت أن يتم استيراد حركة دفتر الأستاذ العام التي نشأت إلى Microsoft Dynamics 365 for Finance and Operations، فيجب أيضًا إعداد حساب Microsoft Azure storage وإدخال سلسلة اتصال Microsoft Azure storage في Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="70f1f-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="70f1f-119">لتشغيل التكامل في Talent، اتبع هذه الخطوات.</span><span class="sxs-lookup"><span data-stu-id="70f1f-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="70f1f-120">في صفحة **إدارة النظام**، حدد **تكوين التكامل**.</span><span class="sxs-lookup"><span data-stu-id="70f1f-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="70f1f-121">أدخل نقطة نهاية بروتوكول نقل الملفات (FTP) الآمنة ومسار مجلد FTP الآمن.</span><span class="sxs-lookup"><span data-stu-id="70f1f-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="70f1f-122">أدخل اسم المستخدم وكلمة المرور للمستخدم الذي سينتقل إلى نقطة النهاية الآمنة ومسار المجلد الآمن في بروتوكول FTP.</span><span class="sxs-lookup"><span data-stu-id="70f1f-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="70f1f-123">اختبر الاتصال، كما تقتضي الحاجة، وعيّن الخيار **تمكين تكامل كشف المرتبات‬** إلى **نعم**.</span><span class="sxs-lookup"><span data-stu-id="70f1f-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="70f1f-124">عند تشغيل التكامل، يتم إنشاء حزمة وملفات تصدير البيانات ويتم تعيين معدل التكرار.</span><span class="sxs-lookup"><span data-stu-id="70f1f-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="70f1f-125">ويمكنك تغيير معدل التكرار وفق الحاجة.</span><span class="sxs-lookup"><span data-stu-id="70f1f-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="70f1f-126">لمزيد من المعلومات حول حسابات مساحة تخزين Azure وسلاسل اتصال مساحة تخزين Azure، راجع موضوعات Azure التالية:</span><span class="sxs-lookup"><span data-stu-id="70f1f-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="70f1f-127">حول حسابات مساحة تخزين Azure</span><span class="sxs-lookup"><span data-stu-id="70f1f-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="70f1f-128">تكوين سلاسل اتصال مساحة تخزين Azure</span><span class="sxs-lookup"><span data-stu-id="70f1f-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="70f1f-129">تكوين بياناتك</span><span class="sxs-lookup"><span data-stu-id="70f1f-129">Configure your data</span></span> 

<span data-ttu-id="70f1f-130">لمعالجة كشف، يجب عليك تكوين بيانات الموارد البشرية في Talent.</span><span class="sxs-lookup"><span data-stu-id="70f1f-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="70f1f-131">يجب إعداد بيانات المؤسسة، مثل الوظائف والمناصب، مع معلومات الميزات والتعويضات.</span><span class="sxs-lookup"><span data-stu-id="70f1f-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="70f1f-132">تتعلق هذه المعلومات بالتوظيف والدفع والخصم وهي معلومات مطلوبة لإنشاء عملية الدفع للموظفين.</span><span class="sxs-lookup"><span data-stu-id="70f1f-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="70f1f-133">بيانات الموارد البشرية</span><span class="sxs-lookup"><span data-stu-id="70f1f-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="70f1f-134">ميزات</span><span class="sxs-lookup"><span data-stu-id="70f1f-134">Benefits</span></span> 

<span data-ttu-id="70f1f-135">توفر الموارد البشرية أدوات يمكن استخدامها لإعداد وحفظ الميزات والخصومات وخطط تعويض العاملين التي تقدمها مؤسسة أو تعالجها للعاملين فيها.</span><span class="sxs-lookup"><span data-stu-id="70f1f-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="70f1f-136">عندما إنشاء ميزات، خذ في الاعتبار البيانات والتكوينات التالية المستخدمة في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="70f1f-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="70f1f-137">خطط الميزات</span><span class="sxs-lookup"><span data-stu-id="70f1f-137">Benefit plans</span></span>

- <span data-ttu-id="70f1f-138">الخطة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="70f1f-138">Plan (required)</span></span>
- <span data-ttu-id="70f1f-139">النوع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-139">Type (required)</span></span>
- <span data-ttu-id="70f1f-140">تأثير كشف المرتبات (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-140">Payroll impact (required)</span></span>
- <span data-ttu-id="70f1f-141">استرداد المتأخرات</span><span class="sxs-lookup"><span data-stu-id="70f1f-141">Recover arrears</span></span>
- <span data-ttu-id="70f1f-142">أسلوب الخصم</span><span class="sxs-lookup"><span data-stu-id="70f1f-142">Deduction method</span></span>
- <span data-ttu-id="70f1f-143">أولوية الخصم</span><span class="sxs-lookup"><span data-stu-id="70f1f-143">Deduction priority</span></span>
- <span data-ttu-id="70f1f-144">حد الفترة</span><span class="sxs-lookup"><span data-stu-id="70f1f-144">Limit period</span></span>
- <span data-ttu-id="70f1f-145">تحديد المبلغ</span><span class="sxs-lookup"><span data-stu-id="70f1f-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="70f1f-146">ميزات</span><span class="sxs-lookup"><span data-stu-id="70f1f-146">Benefits</span></span>

- <span data-ttu-id="70f1f-147">الخطة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="70f1f-147">Plan (required)</span></span>
- <span data-ttu-id="70f1f-148">النوع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-148">Type (required)</span></span>
- <span data-ttu-id="70f1f-149">الخيار (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-149">Option (required)</span></span>
- <span data-ttu-id="70f1f-150">معرّف الميزة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-150">Benefit ID (required)</span></span>
- <span data-ttu-id="70f1f-151">التكرار</span><span class="sxs-lookup"><span data-stu-id="70f1f-151">Frequency</span></span>
- <span data-ttu-id="70f1f-152">أساس</span><span class="sxs-lookup"><span data-stu-id="70f1f-152">Basis</span></span>
- <span data-ttu-id="70f1f-153">المبلغ أو النسبة</span><span class="sxs-lookup"><span data-stu-id="70f1f-153">Amount or rate</span></span>
- <span data-ttu-id="70f1f-154">كود الأرباح</span><span class="sxs-lookup"><span data-stu-id="70f1f-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="70f1f-155">التكرارات المدعومة</span><span class="sxs-lookup"><span data-stu-id="70f1f-155">Supported frequencies</span></span> 

- <span data-ttu-id="70f1f-156">أسبوعيًا</span><span class="sxs-lookup"><span data-stu-id="70f1f-156">Weekly</span></span>
- <span data-ttu-id="70f1f-157">نصف شهري</span><span class="sxs-lookup"><span data-stu-id="70f1f-157">Bi-weekly</span></span>
- <span data-ttu-id="70f1f-158">نصف شهري</span><span class="sxs-lookup"><span data-stu-id="70f1f-158">Semi-monthly</span></span>
- <span data-ttu-id="70f1f-159">شهري</span><span class="sxs-lookup"><span data-stu-id="70f1f-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="70f1f-160">الأسس المدعومة</span><span class="sxs-lookup"><span data-stu-id="70f1f-160">Supported bases</span></span> 

- <span data-ttu-id="70f1f-161">مبلغ ثابت</span><span class="sxs-lookup"><span data-stu-id="70f1f-161">Fixed amount</span></span>
- <span data-ttu-id="70f1f-162">النسبة المئوية للأرباح</span><span class="sxs-lookup"><span data-stu-id="70f1f-162">Percent of earnings</span></span>
- <span data-ttu-id="70f1f-163">ساعات الإنتاج</span><span class="sxs-lookup"><span data-stu-id="70f1f-163">Productive hours</span></span>

<span data-ttu-id="70f1f-164">تنشئ خدمة Dayforce الخصومات التالية، استنادًا إلى تأثير كشف المرتبات المحدد في خطة الميزات.</span><span class="sxs-lookup"><span data-stu-id="70f1f-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="70f1f-165">الاختيار في Talent</span><span class="sxs-lookup"><span data-stu-id="70f1f-165">Selection in Talent</span></span>        | <span data-ttu-id="70f1f-166">النتيجة في Dayforce</span><span class="sxs-lookup"><span data-stu-id="70f1f-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="70f1f-167">بلا</span><span class="sxs-lookup"><span data-stu-id="70f1f-167">None</span></span>                       | <span data-ttu-id="70f1f-168">لا يتم إنشاء أي خصم.</span><span class="sxs-lookup"><span data-stu-id="70f1f-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="70f1f-169">الخصم فقط</span><span class="sxs-lookup"><span data-stu-id="70f1f-169">Deduction only</span></span>             | <span data-ttu-id="70f1f-170">يتم إنشاء خصم الموظف.</span><span class="sxs-lookup"><span data-stu-id="70f1f-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="70f1f-171">المساهمة فقط</span><span class="sxs-lookup"><span data-stu-id="70f1f-171">Contribution only</span></span>          | <span data-ttu-id="70f1f-172">يتم إنشاء خصم صاحب العمل‬.</span><span class="sxs-lookup"><span data-stu-id="70f1f-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="70f1f-173">الخصم والمساهمة</span><span class="sxs-lookup"><span data-stu-id="70f1f-173">Deduction and contribution</span></span> | <span data-ttu-id="70f1f-174">يتم إنشاء خصومات الموظف وصاحب العمل.</span><span class="sxs-lookup"><span data-stu-id="70f1f-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="70f1f-175">لمزيد من المعلومات حول كيفية تحديد وإدارة برنامج ميزات، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="70f1f-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="70f1f-176">تقديم برنامج ميزات الموظفين</span><span class="sxs-lookup"><span data-stu-id="70f1f-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="70f1f-177">إنشاء ميزة جديدة</span><span class="sxs-lookup"><span data-stu-id="70f1f-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="70f1f-178">تحديد قواعد وسياسات استحقاق الفائدة</span><span class="sxs-lookup"><span data-stu-id="70f1f-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="70f1f-179">تسجيل ميزات للعاملين وإزالتها منهم</span><span class="sxs-lookup"><span data-stu-id="70f1f-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="70f1f-180">التعويض</span><span class="sxs-lookup"><span data-stu-id="70f1f-180">Compensation</span></span> 

<span data-ttu-id="70f1f-181">‏‫يتم استخدام إدارة التعويض للتحكم في تسليم الراتب الأساسي والمنح.</span><span class="sxs-lookup"><span data-stu-id="70f1f-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="70f1f-182">ويتم التحكم في دفع الأساس الثابت وزيادات الأهلية للموظف من خلال خطط التعويض الثابت.‬</span><span class="sxs-lookup"><span data-stu-id="70f1f-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="70f1f-183">ويتم التحكم في دفعة دفع الحوافز، مثل دفعات العلاوات، ومكافآت الأداء، وخيارات الأسهم، والمنح، وأيضًا المنح لمرة واحدة، من خلال خطط التعويض المتغير.</span><span class="sxs-lookup"><span data-stu-id="70f1f-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="70f1f-184">تستخدم خدمة Dayforce معلومات التعويض لحساب معدل الموظف السنوي أو الساعي.</span><span class="sxs-lookup"><span data-stu-id="70f1f-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="70f1f-185">وتعتبر خطط التعويض الثابت وتحويلات معدل الدفع مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="70f1f-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="70f1f-186">يجب ربط الموظفين بخطة تعويض ثابت.</span><span class="sxs-lookup"><span data-stu-id="70f1f-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="70f1f-187">لمزيد من المعلومات حول خطط التعويض، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="70f1f-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="70f1f-188">إنشاء خطط التعويض الثابت</span><span class="sxs-lookup"><span data-stu-id="70f1f-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="70f1f-189">إنشاء خطط التعويض المتغير</span><span class="sxs-lookup"><span data-stu-id="70f1f-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="70f1f-190">تطوير خطط وبنية المرتب/التعويض</span><span class="sxs-lookup"><span data-stu-id="70f1f-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="70f1f-191">تعويض العملية</span><span class="sxs-lookup"><span data-stu-id="70f1f-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="70f1f-192">تحديد عملية التعويض وحساب النتائج</span><span class="sxs-lookup"><span data-stu-id="70f1f-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="70f1f-193">تسجيل موظف في خطة تعويض ثابتة</span><span class="sxs-lookup"><span data-stu-id="70f1f-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="70f1f-194">تسجيل موظف في خطة التعويض المتغيرة</span><span class="sxs-lookup"><span data-stu-id="70f1f-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="70f1f-195">الوظائف</span><span class="sxs-lookup"><span data-stu-id="70f1f-195">Jobs</span></span> 

<span data-ttu-id="70f1f-196">الوظيفة هي مجموعة من المهام والمسؤوليات المطلوبة من الشخص الذي يؤدي وظيفة.</span><span class="sxs-lookup"><span data-stu-id="70f1f-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="70f1f-197">لمزيد من المعلومات، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="70f1f-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="70f1f-198">إعداد مكونات وظيفة</span><span class="sxs-lookup"><span data-stu-id="70f1f-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="70f1f-199">تحديد الوظائف الجديدة</span><span class="sxs-lookup"><span data-stu-id="70f1f-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="70f1f-200">المناصب</span><span class="sxs-lookup"><span data-stu-id="70f1f-200">Positions</span></span>

<span data-ttu-id="70f1f-201">يعتبر المنصب مثيلاً فرديًا لوظيفة ما.</span><span class="sxs-lookup"><span data-stu-id="70f1f-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="70f1f-202">على سبيل المثال، المنصب "مدير المبيعات (شرق)،" هو أحد المناصب المقترنة بالوظيفة، "مدير المبيعات".</span><span class="sxs-lookup"><span data-stu-id="70f1f-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="70f1f-203">يوجد منصب في قسم.</span><span class="sxs-lookup"><span data-stu-id="70f1f-203">A position exists in a department.</span></span> <span data-ttu-id="70f1f-204">ويمكن ربط عامل واحد فقط بكل منصب.</span><span class="sxs-lookup"><span data-stu-id="70f1f-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="70f1f-205">عند إعداد المناصب، يجب أخذ البيانات والتكوينات التالية في الاعتبار:</span><span class="sxs-lookup"><span data-stu-id="70f1f-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="70f1f-206">المنصب (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-206">Position (required)</span></span>
- <span data-ttu-id="70f1f-207">الوصف (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-207">Description (required)</span></span>
- <span data-ttu-id="70f1f-208">الوظيف (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="70f1f-208">Job (required)</span></span>
- <span data-ttu-id="70f1f-209">القسم (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-209">Department (required)</span></span>
- <span data-ttu-id="70f1f-210">نوع المنصب (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-210">Position type (required)</span></span>
- <span data-ttu-id="70f1f-211">مكافئ الوقت الكامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-211">Full-time equivalent</span></span>
- <span data-ttu-id="70f1f-212">الساعات العادية السنوية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="70f1f-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="70f1f-213">الدفع بواسطة الكيان القانوني (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="70f1f-214">دورة الدفع (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="70f1f-214">Pay cycle (required)</span></span>
- <span data-ttu-id="70f1f-215">البعد المالي الافتراضي – مركز التكلفة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="70f1f-216">تعيين العامل – العامل وبدء التعيين وانتهاء التعيين وكود السبب</span><span class="sxs-lookup"><span data-stu-id="70f1f-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="70f1f-217">عند ارتباط مناصب متعددة في القسم نفسه بالوظيفة نفسها، فسيتم دمجها في منصب واحد في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="70f1f-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="70f1f-218">لمزيد من المعلومات، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="70f1f-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="70f1f-219">تنظيم قوة العمل باستخدام الإدارات والوظائف والمناصب</span><span class="sxs-lookup"><span data-stu-id="70f1f-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="70f1f-220">إعداد المناصب</span><span class="sxs-lookup"><span data-stu-id="70f1f-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="70f1f-221">الأقسام</span><span class="sxs-lookup"><span data-stu-id="70f1f-221">Departments</span></span>

<span data-ttu-id="70f1f-222">القسم عبارة عن وحدة تشغيل تمثل فئة أو مجال وظيفي في المؤسسة.</span><span class="sxs-lookup"><span data-stu-id="70f1f-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="70f1f-223">والقسم مسؤول عن مجال معين للمؤسسة، مثل المبيعات أو المحاسبة أو الموارد البشرية.</span><span class="sxs-lookup"><span data-stu-id="70f1f-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="70f1f-224">ويمكنك استخدام الأقسام للإبلاغ عن المجالات الوظيفية.</span><span class="sxs-lookup"><span data-stu-id="70f1f-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="70f1f-225">قد تتحمل الأقسام المسؤولية عن الأرباح والخسائر.</span><span class="sxs-lookup"><span data-stu-id="70f1f-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="70f1f-226">لمزيد من المعلومات، راجع الموضوعات التالية:</span><span class="sxs-lookup"><span data-stu-id="70f1f-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="70f1f-227">إنشاء قسم وإقرانه بالتدرج الهرمي للأقسام</span><span class="sxs-lookup"><span data-stu-id="70f1f-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="70f1f-228">تحديد الأقسام الجديدة</span><span class="sxs-lookup"><span data-stu-id="70f1f-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="70f1f-229">دورات الدفع وفترات الدفع</span><span class="sxs-lookup"><span data-stu-id="70f1f-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="70f1f-230">تحدد دورة الدفع معدل تكرار دفع المرتبات والأيام المحددة التي تُدفع فيها الأجور للعاملين.</span><span class="sxs-lookup"><span data-stu-id="70f1f-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="70f1f-231">على سبيل المثال، قد تكون دورة الدفع الشهرية وقد تُدفع الأجور للعاملين في اليوم الأخير من الشهر.</span><span class="sxs-lookup"><span data-stu-id="70f1f-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="70f1f-232">أو، قد تكون دورة الدفع أسبوعية وقد يحصل الموظفون على رواتبهم يوم الثلاثاء بعد انتهاء فترة الدفع.</span><span class="sxs-lookup"><span data-stu-id="70f1f-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="70f1f-233">يتم تعيين دورات الدفع إلى مناصب للتحكم في الوقت الذي يتم فيه دفع أجور العاملين في هذه المناصب.</span><span class="sxs-lookup"><span data-stu-id="70f1f-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="70f1f-234">بعد إنشاء دورات الدفع، يمكنك إنشاء فترات دفع لكل دورة.</span><span class="sxs-lookup"><span data-stu-id="70f1f-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="70f1f-235">تتضمن كل فترة دفع تاريخ دفع افتراضيًا يستند إلى المعلومات التي توفرها.</span><span class="sxs-lookup"><span data-stu-id="70f1f-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="70f1f-236">ومع ذلك، يمكنك تعديل تاريخ الدفع الافتراضي في فترة دفع للسماح بالاستثناءات، مثل عندما يقع تاريخ الدفع يوم عطلة.</span><span class="sxs-lookup"><span data-stu-id="70f1f-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="70f1f-237">يتم استخدام المعلومات التالية في Dayforce:</span><span class="sxs-lookup"><span data-stu-id="70f1f-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="70f1f-238">دورة الدفع (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="70f1f-238">Pay cycle (required)</span></span>
- <span data-ttu-id="70f1f-239">تكرار دورة الدفع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="70f1f-240">تاريخ بدء الفترة (فترة الدفع الأولى مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="70f1f-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="70f1f-241">تاريخ الدفع الافتراضي (فترة الدفع الأولى مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="70f1f-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="70f1f-242">يتم دمج هذه المعلومات مع Dayforce كمجموعات دفع، ويتم فصلها حسب البلد أو المنطقة لكل دورة الدفع.</span><span class="sxs-lookup"><span data-stu-id="70f1f-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="70f1f-243">يجب إنشاء فترة دفع واحدة على الأقل قبل الدمج.</span><span class="sxs-lookup"><span data-stu-id="70f1f-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="70f1f-244">تقوم Dayforce بإنشاء تقويمات وتواريخ دفع للمجموعة، استنادًا إلى تاريخ بدء فترة الدفع الأولى وتاريخ الدفع الافتراضي الذي تم تحديده في Talent.</span><span class="sxs-lookup"><span data-stu-id="70f1f-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="70f1f-245">أكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="70f1f-245">Earning codes</span></span>

<span data-ttu-id="70f1f-246">تحدد أكواد الأرباح بشكل فريد كل نوع من أنواع الأرباح التي يحصل عليها العاملون.</span><span class="sxs-lookup"><span data-stu-id="70f1f-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="70f1f-247">تحتوي أكواد الأرباح على معلمات متنوعة ترتبط بالأرباح، مثل قواعد المحاسبة وقوانين الضرائب ومتطلبات إعداد التقارير وقدرات المبلغ الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="70f1f-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="70f1f-248">يتم استخدام المعلومات التالية في Dayforce:</span><span class="sxs-lookup"><span data-stu-id="70f1f-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="70f1f-249">كود الربح (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-249">Earning Code (required)</span></span>
- <span data-ttu-id="70f1f-250">الوصف</span><span class="sxs-lookup"><span data-stu-id="70f1f-250">Description</span></span>
- <span data-ttu-id="70f1f-251">وحدة القياس</span><span class="sxs-lookup"><span data-stu-id="70f1f-251">Unit of measure</span></span>
- <span data-ttu-id="70f1f-252">منتِج</span><span class="sxs-lookup"><span data-stu-id="70f1f-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="70f1f-253">بيانات العامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-253">Worker data</span></span>

<span data-ttu-id="70f1f-254">تعتبر السجلات الخاصة بمختلف أنواع العاملين مهمة لأنظمة الموارد البشرية وكشوف المرتبات.</span><span class="sxs-lookup"><span data-stu-id="70f1f-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="70f1f-255">يمكن استخدام المعلومات التي تقوم بإدخالها لتعقب العاملين والمعلومات الشخصية.</span><span class="sxs-lookup"><span data-stu-id="70f1f-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="70f1f-256">يمكنك المحافظة على المعلومات التالية للعاملين:</span><span class="sxs-lookup"><span data-stu-id="70f1f-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="70f1f-257">**أساسية** – يمكنك المحافظة على معلومات أساسية حول عامل، مثل معلومات الاتصال والمعلومات الديموغرافية ومعلومات التعريف ومعلومات حول العائلة وحالة الخدمة العسكرية ومعلومات حول المغتربين وجهات الاتصال الشخصية وجهات الاتصال عند الطوارئ.</span><span class="sxs-lookup"><span data-stu-id="70f1f-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="70f1f-258">**التوظيف** – يمكنك المحافظة على معلومات حول توظيف العامل، مثل معلومات حول شركة أو التبعية لمؤسسة وتعيين المنصب وتاريخي البدء والانتهاء والأهلية للعمل وشروط التوظيف والمعاش والإجازة، وتغيير الموقع‬.</span><span class="sxs-lookup"><span data-stu-id="70f1f-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="70f1f-259">**الإجازة والغياب** – يمكنك المحافظة على معلومات حول حالات غياب العامل، مثل تقويمات العمل وحركات الغياب وإعداد الغياب.</span><span class="sxs-lookup"><span data-stu-id="70f1f-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="70f1f-260">**التعويض وكشف المرتبات** – يمكنك المحافظة على معلومات حول خطط تعويض العامل ومعلومات كشف المرتبات، مثل التسجيل في خطة والمكافآت والأداء والعمولة ومعلومات الضريبة والتقاعد والخصومات من الراتب.</span><span class="sxs-lookup"><span data-stu-id="70f1f-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="70f1f-261">عند إدخال معلومات العامل، خذ في الاعتبار البيانات والتكوينات التالية المستخدمة في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="70f1f-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="70f1f-262">معلومات عامة</span><span class="sxs-lookup"><span data-stu-id="70f1f-262">General information</span></span>

- <span data-ttu-id="70f1f-263">رقم الموظف (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-263">Personnel number (required)</span></span>
- <span data-ttu-id="70f1f-264">الاسم الأول (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-264">First name (required)</span></span>
- <span data-ttu-id="70f1f-265">اسم العائلة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-265">Last name (required)</span></span>
- <span data-ttu-id="70f1f-266">الاسم الأوسط</span><span class="sxs-lookup"><span data-stu-id="70f1f-266">Middle name</span></span>
- <span data-ttu-id="70f1f-267">تاريخ الأقدمية</span><span class="sxs-lookup"><span data-stu-id="70f1f-267">Seniority date</span></span>
- <span data-ttu-id="70f1f-268">معروف باسم</span><span class="sxs-lookup"><span data-stu-id="70f1f-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="70f1f-269">معلومات شخصية</span><span class="sxs-lookup"><span data-stu-id="70f1f-269">Personal information</span></span>

- <span data-ttu-id="70f1f-270">الحالة الاجتماعية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="70f1f-270">Marital status (required)</span></span>
- <span data-ttu-id="70f1f-271">تاريخ الميلاد (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-271">Birth date (required)</span></span>
- <span data-ttu-id="70f1f-272">الجنس (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-272">Gender (required)</span></span>
- <span data-ttu-id="70f1f-273">شخص معاق</span><span class="sxs-lookup"><span data-stu-id="70f1f-273">Person with disabilities</span></span>
- <span data-ttu-id="70f1f-274">منطقة/بلد الجنسية (للمكسيك فقط)</span><span class="sxs-lookup"><span data-stu-id="70f1f-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="70f1f-275">معلومات العنوان</span><span class="sxs-lookup"><span data-stu-id="70f1f-275">Address information</span></span>

- <span data-ttu-id="70f1f-276">الأساسي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-276">Primary (required)</span></span>
- <span data-ttu-id="70f1f-277">البلد/المنطقة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-277">Country/region (required)</span></span>
- <span data-ttu-id="70f1f-278">الرمز البريدي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-278">Postal code (required)</span></span>
- <span data-ttu-id="70f1f-279">رقم الشارع (مطلوب) (للمكسيك فقط)</span><span class="sxs-lookup"><span data-stu-id="70f1f-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="70f1f-280">ملحق المبنى (للمكسيك فقط)</span><span class="sxs-lookup"><span data-stu-id="70f1f-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="70f1f-281">المدينة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="70f1f-281">City (required)</span></span>
- <span data-ttu-id="70f1f-282">الولاية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="70f1f-282">State (required)</span></span>
- <span data-ttu-id="70f1f-283">الإقليم (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="70f1f-284">معلومات الاتصال</span><span class="sxs-lookup"><span data-stu-id="70f1f-284">Contact information</span></span> 

- <span data-ttu-id="70f1f-285">الأساسي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-285">Primary (required)</span></span>
- <span data-ttu-id="70f1f-286">رقم الاتصال (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-286">Contact number (required)</span></span>
- <span data-ttu-id="70f1f-287">الرقم الداخلي</span><span class="sxs-lookup"><span data-stu-id="70f1f-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="70f1f-288">معلومات كشف المرتبات وأكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="70f1f-288">Payroll information and earning codes</span></span>

<span data-ttu-id="70f1f-289">قد يتم تعيين أرباح معينة للموظفين عند معدل تكرار دفع معين، وقد تكون لديهم طريقة دفع مفضلة.</span><span class="sxs-lookup"><span data-stu-id="70f1f-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="70f1f-290">يتم استخدام الحقول التالية في Dayforce للمساعدة في ضمان استخدام هذه التفضيلات والإعدادات.</span><span class="sxs-lookup"><span data-stu-id="70f1f-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="70f1f-291">أكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="70f1f-291">Earning codes</span></span>

- <span data-ttu-id="70f1f-292">المنصب (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-292">Position (required)</span></span>
- <span data-ttu-id="70f1f-293">كود الربح (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-293">Earning Code (required)</span></span>
- <span data-ttu-id="70f1f-294">التكرار (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-294">Frequency (required)</span></span>
- <span data-ttu-id="70f1f-295">المبلغ (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="70f1f-296">معلومات الراتب</span><span class="sxs-lookup"><span data-stu-id="70f1f-296">Payroll information</span></span>

- <span data-ttu-id="70f1f-297">طريقة الدفع</span><span class="sxs-lookup"><span data-stu-id="70f1f-297">Payment Method</span></span>
- <span data-ttu-id="70f1f-298">المنطقة الاقتصادية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="70f1f-298">Economic Region (required)</span></span>
- <span data-ttu-id="70f1f-299">معرف ميزات الموظف</span><span class="sxs-lookup"><span data-stu-id="70f1f-299">Employee Benefits ID</span></span>
- <span data-ttu-id="70f1f-300">رقم المعرف القومي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-300">National ID Number (required)</span></span>
- <span data-ttu-id="70f1f-301">رقم الخدمة العسكرية</span><span class="sxs-lookup"><span data-stu-id="70f1f-301">Military Service Number</span></span>
- <span data-ttu-id="70f1f-302">معرف الوردية (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-302">Shift ID (required)</span></span>
- <span data-ttu-id="70f1f-303">رقم الضريبة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-303">Tax Number (required)</span></span>
- <span data-ttu-id="70f1f-304">معرّف الاتحاد (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-304">Union ID (required)</span></span>
- <span data-ttu-id="70f1f-305">معرّف يوم العمل (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-305">Work Day ID (required)</span></span>
- <span data-ttu-id="70f1f-306">رقم تصريح العمل</span><span class="sxs-lookup"><span data-stu-id="70f1f-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="70f1f-307">بالنسبة إلى طريقة الدفع، تدعم المكسيك الدفع **نقدًا** وبواسطة **شيك** (الشيك الفعلي للمؤسسة) و**الدفع الإلكتروني‬**.</span><span class="sxs-lookup"><span data-stu-id="70f1f-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="70f1f-308">إذا لم يتم تحديد أي طريقة دفع، فسيتم استخدام **الشيك** بشكل افتراضي.</span><span class="sxs-lookup"><span data-stu-id="70f1f-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="70f1f-309">تفاصيل التوظيف</span><span class="sxs-lookup"><span data-stu-id="70f1f-309">Employment details</span></span>

<span data-ttu-id="70f1f-310">يتم استخدام سجل تفاصيل التوظيف كمعلومات أساسية لاستخراج حالات تعيين موظف وإنهاء خدماته وإعادة تعيينه في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="70f1f-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="70f1f-311">تدعم خدمة Dayforce سجل توظيف نشط واحد فقط في كل مرة.</span><span class="sxs-lookup"><span data-stu-id="70f1f-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="70f1f-312">تاريخ بدء التوظيف (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-312">Employment start date (required)</span></span>
- <span data-ttu-id="70f1f-313">تاريخ انتهاء التوظيف</span><span class="sxs-lookup"><span data-stu-id="70f1f-313">Employment end date</span></span>
- <span data-ttu-id="70f1f-314">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="70f1f-314">Start date</span></span>
- <span data-ttu-id="70f1f-315">تاريخ البدء المعدل</span><span class="sxs-lookup"><span data-stu-id="70f1f-315">Adjusted start date</span></span>
- <span data-ttu-id="70f1f-316">تاريخ إنهاء الخدمة‬ (مطلوب عند إنهاء الخدمة‬)</span><span class="sxs-lookup"><span data-stu-id="70f1f-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="70f1f-317">سبب إنهاء الخدمة‬ (مطلوب عند إنهاء الخدمة‬)</span><span class="sxs-lookup"><span data-stu-id="70f1f-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="70f1f-318">يتم استخراج التواريخ الأساسية للموظف باستخدام المعلومات التالية.</span><span class="sxs-lookup"><span data-stu-id="70f1f-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="70f1f-319">Talent</span><span class="sxs-lookup"><span data-stu-id="70f1f-319">Talent</span></span>                | <span data-ttu-id="70f1f-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="70f1f-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70f1f-321">أقرب تاريخ توظيف</span><span class="sxs-lookup"><span data-stu-id="70f1f-321">Most recent hire date</span></span> | <span data-ttu-id="70f1f-322">تاريخ بدء التوظيف في سجل محفوظات التوظيف الحالي لموظف لم يتم إنهاء خدماته</span><span class="sxs-lookup"><span data-stu-id="70f1f-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="70f1f-323">تاريخ الإنهاء</span><span class="sxs-lookup"><span data-stu-id="70f1f-323">Termination date</span></span>      | <span data-ttu-id="70f1f-324">تاريخ انتهاء التوظيف في سجل محفوظات التوظيف الحالي لموظف لم يتم إنهاء خدماته</span><span class="sxs-lookup"><span data-stu-id="70f1f-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="70f1f-325">تاريخ البدء</span><span class="sxs-lookup"><span data-stu-id="70f1f-325">Start date</span></span>            | <span data-ttu-id="70f1f-326">تاريخ البدء المعدل أو تاريخ بدء التوظيف في في سجل محفوظات التوظيف الحالي غير النشط</span><span class="sxs-lookup"><span data-stu-id="70f1f-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="70f1f-327">تاريخ التوظيف الأصلي</span><span class="sxs-lookup"><span data-stu-id="70f1f-327">Original hire date</span></span>    | <span data-ttu-id="70f1f-328">تاريخ بدء التوظيف في سجل محفوظات التوظيف الأحدث</span><span class="sxs-lookup"><span data-stu-id="70f1f-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="70f1f-329">التعويض</span><span class="sxs-lookup"><span data-stu-id="70f1f-329">Compensation</span></span>

<span data-ttu-id="70f1f-330">يجب إقران خطة تعويض ثابت بالمنصب الأساسي لكل موظف خلال فترة التوظيف.</span><span class="sxs-lookup"><span data-stu-id="70f1f-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="70f1f-331">تبدأ هذه الفترة الزمنية في التاريخ الذي تم تعيين الموظف فيه (أو تاريخ بدء التوظيف) وتستمر حتى إنهاء خدمة الموظف.</span><span class="sxs-lookup"><span data-stu-id="70f1f-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="70f1f-332">تاريخ السريان (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-332">Effective Date (required)</span></span>
- <span data-ttu-id="70f1f-333">تاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="70f1f-333">Expiration date</span></span>
- <span data-ttu-id="70f1f-334">معدل الدفع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-334">Pay Rate (required)</span></span>
- <span data-ttu-id="70f1f-335">تحويلات ‏‫معدل الدفع (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="70f1f-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="70f1f-336">المكافئ السنوي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="70f1f-337">المكافئ الساعي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="70f1f-338">إذا كان لدى موظف ساعي مناصب متعددة، فسيتم استيراد التعويض الثابت للمنصب الأساسي إلى Dayforce كراتب/معدل أساسي على مستوى الموظف.</span><span class="sxs-lookup"><span data-stu-id="70f1f-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="70f1f-339">فيما يتعلق بالمناصب غير الأساسية، يُحفظ المعدل الساعي إلى المنصب المناظر في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="70f1f-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="70f1f-340">إذا كان لدى موظف يتلقى راتبًا مناصب متعددة، فسيتم استخراج المعدل الساعي التراكمي والراتب السنوي عبر كافة المناصب النشطة، وسيتم استخدامها كراتب/معدل أساسي على مستوى الموظف.</span><span class="sxs-lookup"><span data-stu-id="70f1f-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="70f1f-341">أرقام التعريف</span><span class="sxs-lookup"><span data-stu-id="70f1f-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="70f1f-342">معرّف الضمان الاجتماعي</span><span class="sxs-lookup"><span data-stu-id="70f1f-342">Social Security identifier</span></span> 

<span data-ttu-id="70f1f-343">يجب أن يكون لدى كل موظف معرّفًا أساسيًا.</span><span class="sxs-lookup"><span data-stu-id="70f1f-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="70f1f-344">يجب أن يكون هذا المعرّف من نوع التعريف‬ **SSN**.</span><span class="sxs-lookup"><span data-stu-id="70f1f-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="70f1f-345">في Dayforce، يتم استخراجه تلقائيًا على أنه معرّف الضمان الاجتماعي للموظف المطلوب للتوظيف.</span><span class="sxs-lookup"><span data-stu-id="70f1f-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="70f1f-346">الأساسي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-346">Primary (required)</span></span>
- <span data-ttu-id="70f1f-347">نوع التعريف = "SSN"</span><span class="sxs-lookup"><span data-stu-id="70f1f-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="70f1f-348">تاريخ الإصدار</span><span class="sxs-lookup"><span data-stu-id="70f1f-348">Issued Date</span></span>
- <span data-ttu-id="70f1f-349">تاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="70f1f-349">Expiration Date</span></span>

<span data-ttu-id="70f1f-350">بإمكان الموظفين الإعلان عن أرقام تعريف متعددة من نوع التعريف **SSN**.</span><span class="sxs-lookup"><span data-stu-id="70f1f-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="70f1f-351">ومع ذلك، فإن السجل الذي سيتم دمجه في Dayforce هو فقط الذي يحمل العلامة **أساسي**، بصرف النظر عما إذا كان الرقم نشطًا أو منتهي الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="70f1f-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="70f1f-352">الحسابات البنكية والمدفوعات</span><span class="sxs-lookup"><span data-stu-id="70f1f-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="70f1f-353">يجب إدخال معلومات صالحة حول الحساب البنكي لأي موظف يختار تلقي الدفع من خلال تحويلات إلى الحساب البنكي‬.</span><span class="sxs-lookup"><span data-stu-id="70f1f-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="70f1f-354">Talent</span><span class="sxs-lookup"><span data-stu-id="70f1f-354">Talent</span></span>                         | <span data-ttu-id="70f1f-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="70f1f-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70f1f-356">رقم الحساب البنكي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="70f1f-357">رمز SWIFT (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-357">SWIFT code (required)</span></span>          | <span data-ttu-id="70f1f-358">حقل **معرّف البنك** المستخدم عند معالجة كشف المرتبات في المكسيك.</span><span class="sxs-lookup"><span data-stu-id="70f1f-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="70f1f-359">رقم الفرع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="70f1f-360">نوع الحساب البنكي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-360">Bank account type (required)</span></span>   | <span data-ttu-id="70f1f-361">حقل **نوع البنك** المستخدم عند معالجة كشف المرتبات في المكسيك.</span><span class="sxs-lookup"><span data-stu-id="70f1f-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="70f1f-362">تتضمن القيم المدعومة **شيكات** و**كشف المرتبات**.</span><span class="sxs-lookup"><span data-stu-id="70f1f-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="70f1f-363">يتعين على الموظفين الذين اختاروا تلقي الدفع عبر تحويلات إلى الحساب البنكي‬ توفير ارتباط إلى حساب متبقٍ موجود ضمن كيان قانوني عنوانه الأساسي في المكسيك ويقترن بحساب بنكي صالح من بنك مكسيكي.</span><span class="sxs-lookup"><span data-stu-id="70f1f-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="70f1f-364">يتم تجاهل كافة الحسابات الأخرى غير الحسابات المتبقية.</span><span class="sxs-lookup"><span data-stu-id="70f1f-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="70f1f-365">معلومات العنوان</span><span class="sxs-lookup"><span data-stu-id="70f1f-365">Address information</span></span>

<span data-ttu-id="70f1f-366">يجب أن يكون لدى كل موظف موقعًا أساسيًا.</span><span class="sxs-lookup"><span data-stu-id="70f1f-366">Every employee must have one primary location.</span></span> <span data-ttu-id="70f1f-367">في Dayforce، يتم استخدام هذا الموقع لتحديد مكان الإقامة الأساسي للموظف لأغراض ضريبية.</span><span class="sxs-lookup"><span data-stu-id="70f1f-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="70f1f-368">الأساسي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-368">Primary (required)</span></span>
- <span data-ttu-id="70f1f-369">البلد/المنطقة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-369">Country/region (required)</span></span>
- <span data-ttu-id="70f1f-370">الرمز البريدي (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="70f1f-371">الشارع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-371">Street (required)</span></span>
- <span data-ttu-id="70f1f-372">رقم الشارع (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-372">Street Number (required)</span></span>
- <span data-ttu-id="70f1f-373">ملحق المبنى</span><span class="sxs-lookup"><span data-stu-id="70f1f-373">Building Complement</span></span>
- <span data-ttu-id="70f1f-374">المدينة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="70f1f-374">City (required)</span></span>
- <span data-ttu-id="70f1f-375">الولاية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="70f1f-375">State (required)</span></span>
- <span data-ttu-id="70f1f-376">الإقليم (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="70f1f-377">تكوين البيانات لإنشاء كشف مرتبات في الولايات المتحدة وكندا</span><span class="sxs-lookup"><span data-stu-id="70f1f-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="70f1f-378">إذا كنت تقوم بإنشاء الدفع للموظفين في الولايات المتحدة وكندا، يجب أن يتم تكوين العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="70f1f-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="70f1f-379">الأقسام مطلوبة على المناصب.</span><span class="sxs-lookup"><span data-stu-id="70f1f-379">Departments are required on positions.</span></span>
- <span data-ttu-id="70f1f-380">يجب تعيين مراكز التكلفة كأبعاد مالية ويجب أن تكون العنصر الأول في سلسلة الأبعاد المالية الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="70f1f-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="70f1f-381">أنواع الوظيفة</span><span class="sxs-lookup"><span data-stu-id="70f1f-381">Job types</span></span>

<span data-ttu-id="70f1f-382">يتم استخدام أنواع الوظائف لتجميع وظائف مماثلة في فئات.</span><span class="sxs-lookup"><span data-stu-id="70f1f-382">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="70f1f-383">تعتبر أنواع الوظائف مطلوبة لمعالجة كشف المرتبات في الولايات المتحدة وكندا.</span><span class="sxs-lookup"><span data-stu-id="70f1f-383">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="70f1f-384">تتضمن أمثلة عن أنواع الوظائف الدوام الكامل والدوام الجزئي أو الراتب والدفع بالساعة.</span><span class="sxs-lookup"><span data-stu-id="70f1f-384">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="70f1f-385">يتم تعيين أنواع الوظائف إلى Dayforce كأنواع دفع تشير إلى ما إذا كان الموظف يتقاضى أجره بالساعة أو يتقاضى راتبًا.</span><span class="sxs-lookup"><span data-stu-id="70f1f-385">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="70f1f-386">أنواع الوظائف التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="70f1f-386">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="70f1f-387">نوع الوظيفة</span><span class="sxs-lookup"><span data-stu-id="70f1f-387">Job type</span></span>   | <span data-ttu-id="70f1f-388">الوصف</span><span class="sxs-lookup"><span data-stu-id="70f1f-388">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="70f1f-389">كل ساعة</span><span class="sxs-lookup"><span data-stu-id="70f1f-389">Hourly</span></span>     | <span data-ttu-id="70f1f-390">كل ساعة</span><span class="sxs-lookup"><span data-stu-id="70f1f-390">Hourly</span></span>      |
| <span data-ttu-id="70f1f-391">يتقاضى راتبًا</span><span class="sxs-lookup"><span data-stu-id="70f1f-391">Salaried</span></span>   | <span data-ttu-id="70f1f-392">يتقاضى راتبًا</span><span class="sxs-lookup"><span data-stu-id="70f1f-392">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="70f1f-393">أنواع المناصب</span><span class="sxs-lookup"><span data-stu-id="70f1f-393">Position types</span></span> 

<span data-ttu-id="70f1f-394">يمكنك استخدام أنواع المناصب لوصف ما إذا كانت المناصب عبارة عن دوام كامل أو دوام جزئي أو شيء آخر.</span><span class="sxs-lookup"><span data-stu-id="70f1f-394">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="70f1f-395">يتم تعيين أنواع المناصب إلى Dayforce كفئات دفع تشير إلى ما إذا كان الموظف يعمل بدوام كامل أو دوام جزئي.</span><span class="sxs-lookup"><span data-stu-id="70f1f-395">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="70f1f-396">أنواع المناصب التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="70f1f-396">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="70f1f-397">نوع المنصب</span><span class="sxs-lookup"><span data-stu-id="70f1f-397">Position type</span></span>   | <span data-ttu-id="70f1f-398">الوصف</span><span class="sxs-lookup"><span data-stu-id="70f1f-398">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="70f1f-399">دوام كامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-399">Full-time</span></span>       | <span data-ttu-id="70f1f-400">موظف بدوام كامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-400">Full time employee</span></span> |
| <span data-ttu-id="70f1f-401">دوام جزئي</span><span class="sxs-lookup"><span data-stu-id="70f1f-401">Part-time</span></span>       | <span data-ttu-id="70f1f-402">موظف بدوام جزئي</span><span class="sxs-lookup"><span data-stu-id="70f1f-402">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="70f1f-403">رموز السبب</span><span class="sxs-lookup"><span data-stu-id="70f1f-403">Reason codes</span></span>

<span data-ttu-id="70f1f-404">توفير أكواد الأسباب معلومات حول حالة الموظف.</span><span class="sxs-lookup"><span data-stu-id="70f1f-404">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="70f1f-405">يتم تعيين أكواد الأسباب إلى Dayforce كأسباب الحالة للإشارة إلى السبب الذي يكمن خلف التغييرات في منصب الموظف أو حالة توظيفه.</span><span class="sxs-lookup"><span data-stu-id="70f1f-405">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="70f1f-406">أكواد الأسباب التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="70f1f-406">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="70f1f-407">رمز السبب</span><span class="sxs-lookup"><span data-stu-id="70f1f-407">Reason code</span></span>    | <span data-ttu-id="70f1f-408">الوصف</span><span class="sxs-lookup"><span data-stu-id="70f1f-408">Description</span></span>      | <span data-ttu-id="70f1f-409">السيناريوهات القابلة للتطبيق</span><span class="sxs-lookup"><span data-stu-id="70f1f-409">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="70f1f-410">الاستقالة</span><span class="sxs-lookup"><span data-stu-id="70f1f-410">RESIGNATION</span></span>    | <span data-ttu-id="70f1f-411">الاستقالة</span><span class="sxs-lookup"><span data-stu-id="70f1f-411">Resignation</span></span>      | <span data-ttu-id="70f1f-412">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-412">Terminate worker</span></span>     |
| <span data-ttu-id="70f1f-413">إنهاء الخدمة</span><span class="sxs-lookup"><span data-stu-id="70f1f-413">TERMINATION</span></span>    | <span data-ttu-id="70f1f-414">إنهاء الخدمة</span><span class="sxs-lookup"><span data-stu-id="70f1f-414">Termination</span></span>      | <span data-ttu-id="70f1f-415">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-415">Terminate worker</span></span>     |
| <span data-ttu-id="70f1f-416">التقاعد</span><span class="sxs-lookup"><span data-stu-id="70f1f-416">RETIREMENT</span></span>     | <span data-ttu-id="70f1f-417">التقاعد</span><span class="sxs-lookup"><span data-stu-id="70f1f-417">Retirement</span></span>       | <span data-ttu-id="70f1f-418">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-418">Terminate worker</span></span>     |
| <span data-ttu-id="70f1f-419">‏‏غير ذلك</span><span class="sxs-lookup"><span data-stu-id="70f1f-419">OTHER</span></span>          | <span data-ttu-id="70f1f-420">أسباب أخرى</span><span class="sxs-lookup"><span data-stu-id="70f1f-420">Other Reasons</span></span>    | <span data-ttu-id="70f1f-421">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-421">Terminate worker</span></span>     |
| <span data-ttu-id="70f1f-422">الوفاة</span><span class="sxs-lookup"><span data-stu-id="70f1f-422">DEATH</span></span>          | <span data-ttu-id="70f1f-423">الوفاة</span><span class="sxs-lookup"><span data-stu-id="70f1f-423">Death</span></span>            | <span data-ttu-id="70f1f-424">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-424">Terminate worker</span></span>     |
| <span data-ttu-id="70f1f-425">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="70f1f-425">LEAVEOFABSENCE</span></span> | <span data-ttu-id="70f1f-426">إذن غياب</span><span class="sxs-lookup"><span data-stu-id="70f1f-426">Leave of Absence</span></span> | <span data-ttu-id="70f1f-427">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-427">Terminate worker</span></span>     |
| <span data-ttu-id="70f1f-428">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="70f1f-428">CONTRACTEND</span></span>    | <span data-ttu-id="70f1f-429">انتهاء العقد</span><span class="sxs-lookup"><span data-stu-id="70f1f-429">End of Contract</span></span>  | <span data-ttu-id="70f1f-430">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-430">Terminate worker</span></span>     |
| <span data-ttu-id="70f1f-431">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="70f1f-431">SALARYCHANGE</span></span>   | <span data-ttu-id="70f1f-432">تغيير الراتب</span><span class="sxs-lookup"><span data-stu-id="70f1f-432">Change of Salary</span></span> | <span data-ttu-id="70f1f-433">التعويض</span><span class="sxs-lookup"><span data-stu-id="70f1f-433">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="70f1f-434">الحالة الاجتماعية</span><span class="sxs-lookup"><span data-stu-id="70f1f-434">Marital status</span></span>

<span data-ttu-id="70f1f-435">يتم تعيين قيم الحالة الاجتماعية إلى Dayforce وترجمتها، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="70f1f-435">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="70f1f-436">يعرض الجدول التالي كيفية تعيين قيم الحالة الاجتماعية إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="70f1f-436">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="70f1f-437">Talent</span><span class="sxs-lookup"><span data-stu-id="70f1f-437">Talent</span></span>                 | <span data-ttu-id="70f1f-438">Dayforce</span><span class="sxs-lookup"><span data-stu-id="70f1f-438">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="70f1f-439">متزوج</span><span class="sxs-lookup"><span data-stu-id="70f1f-439">Married</span></span>                | <span data-ttu-id="70f1f-440">متزوج</span><span class="sxs-lookup"><span data-stu-id="70f1f-440">Married</span></span>              |
| <span data-ttu-id="70f1f-441">واحد</span><span class="sxs-lookup"><span data-stu-id="70f1f-441">Single</span></span>                 | <span data-ttu-id="70f1f-442">واحد</span><span class="sxs-lookup"><span data-stu-id="70f1f-442">Single</span></span>               |
| <span data-ttu-id="70f1f-443">أرمل</span><span class="sxs-lookup"><span data-stu-id="70f1f-443">Widowed</span></span>                | <span data-ttu-id="70f1f-444">أرمل</span><span class="sxs-lookup"><span data-stu-id="70f1f-444">Widowed</span></span>              |
| <span data-ttu-id="70f1f-445">مطلق</span><span class="sxs-lookup"><span data-stu-id="70f1f-445">Divorced</span></span>               | <span data-ttu-id="70f1f-446">مطلق</span><span class="sxs-lookup"><span data-stu-id="70f1f-446">Divorced</span></span>             |
| <span data-ttu-id="70f1f-447">شراكة مسجلة</span><span class="sxs-lookup"><span data-stu-id="70f1f-447">Registered Partnership</span></span> | <span data-ttu-id="70f1f-448">الشراكة المحلية</span><span class="sxs-lookup"><span data-stu-id="70f1f-448">Domestic Partnership</span></span> |
| <span data-ttu-id="70f1f-449">بلا</span><span class="sxs-lookup"><span data-stu-id="70f1f-449">None</span></span>                   | <span data-ttu-id="70f1f-450">بلا</span><span class="sxs-lookup"><span data-stu-id="70f1f-450">None</span></span>                 |
| <span data-ttu-id="70f1f-451">تعايش</span><span class="sxs-lookup"><span data-stu-id="70f1f-451">Cohabiting</span></span>             | <span data-ttu-id="70f1f-452">تعايش</span><span class="sxs-lookup"><span data-stu-id="70f1f-452">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="70f1f-453">الجنس</span><span class="sxs-lookup"><span data-stu-id="70f1f-453">Gender</span></span>

<span data-ttu-id="70f1f-454">يتم تعيين الجنس إلى Dayforce وترجمته، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="70f1f-454">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="70f1f-455">يعرض الجدول التالي كيفية تعيين الجنس إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="70f1f-455">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="70f1f-456">Talent</span><span class="sxs-lookup"><span data-stu-id="70f1f-456">Talent</span></span>       | <span data-ttu-id="70f1f-457">Dayforce</span><span class="sxs-lookup"><span data-stu-id="70f1f-457">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="70f1f-458">ذكر</span><span class="sxs-lookup"><span data-stu-id="70f1f-458">Male</span></span>         | <span data-ttu-id="70f1f-459">ذكر</span><span class="sxs-lookup"><span data-stu-id="70f1f-459">Male</span></span>            |
| <span data-ttu-id="70f1f-460">أنثى</span><span class="sxs-lookup"><span data-stu-id="70f1f-460">Female</span></span>       | <span data-ttu-id="70f1f-461">أنثى</span><span class="sxs-lookup"><span data-stu-id="70f1f-461">Female</span></span>          |
| <span data-ttu-id="70f1f-462">غير محدد</span><span class="sxs-lookup"><span data-stu-id="70f1f-462">Non-specific</span></span> | <span data-ttu-id="70f1f-463">*غير مدعوم*</span><span class="sxs-lookup"><span data-stu-id="70f1f-463">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="70f1f-464">أكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="70f1f-464">Earning codes</span></span>

<span data-ttu-id="70f1f-465">تحدد أكواد الأرباح بشكل فريد كل نوع من أنواع الأرباح التي يحصل عليها العاملون.</span><span class="sxs-lookup"><span data-stu-id="70f1f-465">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="70f1f-466">تغطي الأكواد معلمات متنوعة ترتبط بالأرباح، مثل قواعد المحاسبة وقوانين الضرائب ومتطلبات إعداد التقارير وقدرات المبلغ الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="70f1f-466">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="70f1f-467">إذا تم استخدام تكرار غير معتمد، يُستخدم التكرار **كل عملية دفع** بشكل افتراضي للحساب.</span><span class="sxs-lookup"><span data-stu-id="70f1f-467">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="70f1f-468">التكرارات المدعومة</span><span class="sxs-lookup"><span data-stu-id="70f1f-468">Supported frequencies</span></span>

- <span data-ttu-id="70f1f-469">الكل</span><span class="sxs-lookup"><span data-stu-id="70f1f-469">All</span></span>
- <span data-ttu-id="70f1f-470">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="70f1f-470">EVERYPAY</span></span>
- <span data-ttu-id="70f1f-471">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="70f1f-471">EACHPAYPERIOD</span></span>
- <span data-ttu-id="70f1f-472">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="70f1f-472">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="70f1f-473">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="70f1f-473">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="70f1f-474">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-474">1OFMTH</span></span>
- <span data-ttu-id="70f1f-475">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-475">LASTOFMTH</span></span>
- <span data-ttu-id="70f1f-476">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-476">2OFMTH</span></span>
- <span data-ttu-id="70f1f-477">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-477">3OFMTH</span></span>
- <span data-ttu-id="70f1f-478">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-478">4OFMTH</span></span>
- <span data-ttu-id="70f1f-479">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-479">5OFMTH</span></span>
- <span data-ttu-id="70f1f-480">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-480">1N2OFMTH</span></span>
- <span data-ttu-id="70f1f-481">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-481">3N4OFMTH</span></span>
- <span data-ttu-id="70f1f-482">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-482">1N3OFMTH</span></span>
- <span data-ttu-id="70f1f-483">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-483">1N4OFMTH</span></span>
- <span data-ttu-id="70f1f-484">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-484">2N3OFMTH</span></span>
- <span data-ttu-id="70f1f-485">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-485">2N4OFMTH</span></span>
- <span data-ttu-id="70f1f-486">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-486">1N2N3OFMTH</span></span>
- <span data-ttu-id="70f1f-487">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-487">1N2N4OFMTH</span></span>
- <span data-ttu-id="70f1f-488">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-488">1N3N4OFMTH</span></span>
- <span data-ttu-id="70f1f-489">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-489">2N3N4OFMTH</span></span>
- <span data-ttu-id="70f1f-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="70f1f-491">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="70f1f-491">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="70f1f-492">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="70f1f-492">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="70f1f-493">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="70f1f-493">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="70f1f-494">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="70f1f-494">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="70f1f-495">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="70f1f-495">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="70f1f-496">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="70f1f-496">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="70f1f-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="70f1f-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="70f1f-498">العناوين</span><span class="sxs-lookup"><span data-stu-id="70f1f-498">Addresses</span></span>

<span data-ttu-id="70f1f-499">يتطلب تعريف أكواد بلد أو منطقة وولاية وإقليم (بلدية) معينة تنسيقات معينة تستطيع Dayforce والموفرين في البلد/في المنطقة التعرف عليها.</span><span class="sxs-lookup"><span data-stu-id="70f1f-499">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="70f1f-500">على الرغم من أن تنسيق المدن يعتبر مرنًا، يجب أن تكون كل مدينة مقترنة بولاية.</span><span class="sxs-lookup"><span data-stu-id="70f1f-500">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="70f1f-501">Talent</span><span class="sxs-lookup"><span data-stu-id="70f1f-501">Talent</span></span>          | <span data-ttu-id="70f1f-502">Dayforce</span><span class="sxs-lookup"><span data-stu-id="70f1f-502">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="70f1f-503">البلد/المنطقة</span><span class="sxs-lookup"><span data-stu-id="70f1f-503">Country/Region</span></span>  | <span data-ttu-id="70f1f-504">كود البلد</span><span class="sxs-lookup"><span data-stu-id="70f1f-504">Country Code</span></span>          |
| <span data-ttu-id="70f1f-505">الرمز البريدي</span><span class="sxs-lookup"><span data-stu-id="70f1f-505">Zip/Postal Code</span></span> | <span data-ttu-id="70f1f-506">الرمز البريدي</span><span class="sxs-lookup"><span data-stu-id="70f1f-506">Postal Code</span></span>           |
| <span data-ttu-id="70f1f-507">المنطقة‬</span><span class="sxs-lookup"><span data-stu-id="70f1f-507">State</span></span>           | <span data-ttu-id="70f1f-508">كود الولاية</span><span class="sxs-lookup"><span data-stu-id="70f1f-508">State Code</span></span>            |
| <span data-ttu-id="70f1f-509">المدينة</span><span class="sxs-lookup"><span data-stu-id="70f1f-509">City</span></span>            | <span data-ttu-id="70f1f-510">المدينة</span><span class="sxs-lookup"><span data-stu-id="70f1f-510">City</span></span>                  |
| <span data-ttu-id="70f1f-511">الإقليم</span><span class="sxs-lookup"><span data-stu-id="70f1f-511">County</span></span>          | <span data-ttu-id="70f1f-512">المقاطعة (بلدية)</span><span class="sxs-lookup"><span data-stu-id="70f1f-512">County (Municipality)</span></span> |
| <span data-ttu-id="70f1f-513">الشارع</span><span class="sxs-lookup"><span data-stu-id="70f1f-513">Street</span></span>          | <span data-ttu-id="70f1f-514">سطر العنوان 1</span><span class="sxs-lookup"><span data-stu-id="70f1f-514">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="70f1f-515">مناطق الضريبة</span><span class="sxs-lookup"><span data-stu-id="70f1f-515">Tax regions</span></span>

<span data-ttu-id="70f1f-516">تُستخدم مناطق الضريبة لتحديد الضريبة المناسبة التي يجب تطبيقها أثناء إنشاء كشف المرتبات.</span><span class="sxs-lookup"><span data-stu-id="70f1f-516">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="70f1f-517">يتم تعيين مناطق الضريبة إلى Dayforce كعناوين موقع.</span><span class="sxs-lookup"><span data-stu-id="70f1f-517">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="70f1f-518">يجب أن تكون منطقة الضريبة الافتراضية مقترنة بمنصب العامل النشط.</span><span class="sxs-lookup"><span data-stu-id="70f1f-518">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="70f1f-519">منطقة الضريبة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="70f1f-519">Tax region (required)</span></span>
- <span data-ttu-id="70f1f-520">البلد/المنطقة (مطلوب)</span><span class="sxs-lookup"><span data-stu-id="70f1f-520">Country/Region (required)</span></span>
- <span data-ttu-id="70f1f-521">الولاية (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="70f1f-521">State (required)</span></span>
- <span data-ttu-id="70f1f-522">الإقليم</span><span class="sxs-lookup"><span data-stu-id="70f1f-522">County</span></span> 
- <span data-ttu-id="70f1f-523">المدينة (مطلوبة)</span><span class="sxs-lookup"><span data-stu-id="70f1f-523">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="70f1f-524">تكوين بياناتك لإنشاء كشف المرتبات في المكسيك</span><span class="sxs-lookup"><span data-stu-id="70f1f-524">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="70f1f-525">إذا كنت تقوم بإنشاء الدفع للموظفين في المكسيك، يجب أن يتم تكوين العناصر التالية:</span><span class="sxs-lookup"><span data-stu-id="70f1f-525">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="70f1f-526">الأقسام مطلوبة على المناصب.</span><span class="sxs-lookup"><span data-stu-id="70f1f-526">Departments are required on positions.</span></span>
- <span data-ttu-id="70f1f-527">يجب تعيين مراكز التكلفة كأبعاد مالية ويجب أن تكون العنصر الأول في سلسلة الأبعاد المالية الافتراضية.</span><span class="sxs-lookup"><span data-stu-id="70f1f-527">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="70f1f-528">أنواع الوظيفة</span><span class="sxs-lookup"><span data-stu-id="70f1f-528">Job types</span></span>

<span data-ttu-id="70f1f-529">يتم استخدام أنواع الوظائف لتجميع وظائف مماثلة في فئات.</span><span class="sxs-lookup"><span data-stu-id="70f1f-529">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="70f1f-530">أنواع الوظائف مطلوبة لمعالجة كشف المرتبات في المكسيك.</span><span class="sxs-lookup"><span data-stu-id="70f1f-530">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="70f1f-531">تتضمن أمثلة عن أنواع الوظائف الدوام الكامل والدوام الجزئي أو الراتب والدفع بالساعة.</span><span class="sxs-lookup"><span data-stu-id="70f1f-531">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="70f1f-532">يتم تعيين أنواع الوظائف إلى Dayforce كأنواع دفع تشير إلى ما إذا كان الموظف يتقاضى أجره بالساعة أو يتقاضى راتبًا.</span><span class="sxs-lookup"><span data-stu-id="70f1f-532">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="70f1f-533">أنواع الوظائف التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="70f1f-533">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="70f1f-534">نوع الوظيفة</span><span class="sxs-lookup"><span data-stu-id="70f1f-534">Job type</span></span>   | <span data-ttu-id="70f1f-535">الوصف</span><span class="sxs-lookup"><span data-stu-id="70f1f-535">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="70f1f-536">كل ساعة</span><span class="sxs-lookup"><span data-stu-id="70f1f-536">Hourly</span></span>     | <span data-ttu-id="70f1f-537">الحد الأقصى للأجر في الساعة‬</span><span class="sxs-lookup"><span data-stu-id="70f1f-537">MX Hourly</span></span>   |
| <span data-ttu-id="70f1f-538">يتقاضى راتبًا</span><span class="sxs-lookup"><span data-stu-id="70f1f-538">Salaried</span></span>   | <span data-ttu-id="70f1f-539">الحد الأقصى للراتب</span><span class="sxs-lookup"><span data-stu-id="70f1f-539">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="70f1f-540">أنواع المناصب</span><span class="sxs-lookup"><span data-stu-id="70f1f-540">Position types</span></span> 

<span data-ttu-id="70f1f-541">يمكنك استخدام أنواع المناصب لوصف ما إذا كانت المناصب عبارة عن دوام كامل أو دوام جزئي أو شيء آخر.</span><span class="sxs-lookup"><span data-stu-id="70f1f-541">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="70f1f-542">يتم تعيين أنواع المناصب إلى Dayforce كفئات دفع تشير إلى ما إذا كان الموظف يعمل بدوام كامل أو دوام جزئي.</span><span class="sxs-lookup"><span data-stu-id="70f1f-542">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="70f1f-543">أنواع المناصب التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="70f1f-543">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="70f1f-544">نوع المنصب</span><span class="sxs-lookup"><span data-stu-id="70f1f-544">Position type</span></span>   | <span data-ttu-id="70f1f-545">الوصف</span><span class="sxs-lookup"><span data-stu-id="70f1f-545">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="70f1f-546">دوام كامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-546">Full-time</span></span>       | <span data-ttu-id="70f1f-547">موظف بدوام كامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-547">Full time employee</span></span> |
| <span data-ttu-id="70f1f-548">دوام جزئي</span><span class="sxs-lookup"><span data-stu-id="70f1f-548">Part-time</span></span>       | <span data-ttu-id="70f1f-549">موظف بدوام جزئي</span><span class="sxs-lookup"><span data-stu-id="70f1f-549">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="70f1f-550">رموز السبب</span><span class="sxs-lookup"><span data-stu-id="70f1f-550">Reason codes</span></span>

<span data-ttu-id="70f1f-551">توفير أكواد الأسباب معلومات حول حالة الموظف.</span><span class="sxs-lookup"><span data-stu-id="70f1f-551">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="70f1f-552">يتم تعيين أكواد الأسباب إلى Dayforce كأسباب الحالة للإشارة إلى السبب الذي يكمن خلف التغييرات في منصب الموظف أو حالة توظيفه.</span><span class="sxs-lookup"><span data-stu-id="70f1f-552">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="70f1f-553">أكواد الأسباب التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="70f1f-553">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="70f1f-554">رمز السبب</span><span class="sxs-lookup"><span data-stu-id="70f1f-554">Reason code</span></span>            | <span data-ttu-id="70f1f-555">الوصف</span><span class="sxs-lookup"><span data-stu-id="70f1f-555">Description</span></span>                    | <span data-ttu-id="70f1f-556">السيناريوهات القابلة للتطبيق</span><span class="sxs-lookup"><span data-stu-id="70f1f-556">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="70f1f-557">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="70f1f-557">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="70f1f-558">المغادرة قبل كشف المرتبات الأول</span><span class="sxs-lookup"><span data-stu-id="70f1f-558">Departure before first payroll</span></span> | <span data-ttu-id="70f1f-559">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-559">Terminate worker</span></span>     |
| <span data-ttu-id="70f1f-560">الاستقالة</span><span class="sxs-lookup"><span data-stu-id="70f1f-560">RESIGNATION</span></span>            | <span data-ttu-id="70f1f-561">الاستقالة</span><span class="sxs-lookup"><span data-stu-id="70f1f-561">Resignation</span></span>                    | <span data-ttu-id="70f1f-562">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-562">Terminate worker</span></span>     |
| <span data-ttu-id="70f1f-563">المعاش</span><span class="sxs-lookup"><span data-stu-id="70f1f-563">PENSION</span></span>                | <span data-ttu-id="70f1f-564">المعاش</span><span class="sxs-lookup"><span data-stu-id="70f1f-564">Pension</span></span>                        | <span data-ttu-id="70f1f-565">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-565">Terminate worker</span></span>     |
| <span data-ttu-id="70f1f-566">إنهاء الخدمة</span><span class="sxs-lookup"><span data-stu-id="70f1f-566">TERMINATION</span></span>            | <span data-ttu-id="70f1f-567">إنهاء الخدمة</span><span class="sxs-lookup"><span data-stu-id="70f1f-567">Termination</span></span>                    | <span data-ttu-id="70f1f-568">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-568">Terminate worker</span></span>     |
| <span data-ttu-id="70f1f-569">التقاعد</span><span class="sxs-lookup"><span data-stu-id="70f1f-569">RETIREMENT</span></span>             | <span data-ttu-id="70f1f-570">التقاعد</span><span class="sxs-lookup"><span data-stu-id="70f1f-570">Retirement</span></span>                     | <span data-ttu-id="70f1f-571">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-571">Terminate worker</span></span>     |
| <span data-ttu-id="70f1f-572">الغائب</span><span class="sxs-lookup"><span data-stu-id="70f1f-572">ABSENTEE</span></span>               | <span data-ttu-id="70f1f-573">الغائب</span><span class="sxs-lookup"><span data-stu-id="70f1f-573">Absentee</span></span>                       | <span data-ttu-id="70f1f-574">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-574">Terminate worker</span></span>     |
| <span data-ttu-id="70f1f-575">‏‏غير ذلك</span><span class="sxs-lookup"><span data-stu-id="70f1f-575">OTHER</span></span>                  | <span data-ttu-id="70f1f-576">أسباب أخرى</span><span class="sxs-lookup"><span data-stu-id="70f1f-576">Other Reasons</span></span>                  | <span data-ttu-id="70f1f-577">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-577">Terminate worker</span></span>     |
| <span data-ttu-id="70f1f-578">إقفال</span><span class="sxs-lookup"><span data-stu-id="70f1f-578">CLOSURE</span></span>                | <span data-ttu-id="70f1f-579">إقفال الشركة</span><span class="sxs-lookup"><span data-stu-id="70f1f-579">Business Closure</span></span>               | <span data-ttu-id="70f1f-580">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-580">Terminate worker</span></span>     |
| <span data-ttu-id="70f1f-581">الوفاة</span><span class="sxs-lookup"><span data-stu-id="70f1f-581">DEATH</span></span>                  | <span data-ttu-id="70f1f-582">الوفاة</span><span class="sxs-lookup"><span data-stu-id="70f1f-582">Death</span></span>                          | <span data-ttu-id="70f1f-583">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-583">Terminate worker</span></span>     |
| <span data-ttu-id="70f1f-584">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="70f1f-584">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="70f1f-585">إذن غياب</span><span class="sxs-lookup"><span data-stu-id="70f1f-585">Leave of Absence</span></span>               | <span data-ttu-id="70f1f-586">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-586">Terminate worker</span></span>     |
| <span data-ttu-id="70f1f-587">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="70f1f-587">CONTRACTEND</span></span>            | <span data-ttu-id="70f1f-588">انتهاء العقد</span><span class="sxs-lookup"><span data-stu-id="70f1f-588">End of Contract</span></span>                | <span data-ttu-id="70f1f-589">فصل العامل</span><span class="sxs-lookup"><span data-stu-id="70f1f-589">Terminate worker</span></span>     |
| <span data-ttu-id="70f1f-590">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="70f1f-590">SALARYCHANGE</span></span>           | <span data-ttu-id="70f1f-591">تغيير الراتب</span><span class="sxs-lookup"><span data-stu-id="70f1f-591">Change of Salary</span></span>               | <span data-ttu-id="70f1f-592">التعويض</span><span class="sxs-lookup"><span data-stu-id="70f1f-592">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="70f1f-593">شروط التوظيف</span><span class="sxs-lookup"><span data-stu-id="70f1f-593">Terms of employment</span></span>

<span data-ttu-id="70f1f-594">يتم استخدام شروط التوظيف لإنشاء فئات شروط التوظيف.</span><span class="sxs-lookup"><span data-stu-id="70f1f-594">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="70f1f-595">يتم تعيين الشروط إلى Dayforce كقيم مؤشر التوظيف.</span><span class="sxs-lookup"><span data-stu-id="70f1f-595">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="70f1f-596">شروط التوظيف التالية وأوصافها مطلوبة.</span><span class="sxs-lookup"><span data-stu-id="70f1f-596">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="70f1f-597">شروط التوظيف</span><span class="sxs-lookup"><span data-stu-id="70f1f-597">Terms of employment</span></span>   | <span data-ttu-id="70f1f-598">الوصف</span><span class="sxs-lookup"><span data-stu-id="70f1f-598">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="70f1f-599">عادي</span><span class="sxs-lookup"><span data-stu-id="70f1f-599">Regular</span></span>               | <span data-ttu-id="70f1f-600">عادي</span><span class="sxs-lookup"><span data-stu-id="70f1f-600">Regular</span></span>     |
| <span data-ttu-id="70f1f-601">مباشر</span><span class="sxs-lookup"><span data-stu-id="70f1f-601">Direct</span></span>                | <span data-ttu-id="70f1f-602">مباشر</span><span class="sxs-lookup"><span data-stu-id="70f1f-602">Direct</span></span>      |
| <span data-ttu-id="70f1f-603">فترة تدريب</span><span class="sxs-lookup"><span data-stu-id="70f1f-603">Internship</span></span>            | <span data-ttu-id="70f1f-604">فترة تدريب</span><span class="sxs-lookup"><span data-stu-id="70f1f-604">Internship</span></span>  |
| <span data-ttu-id="70f1f-605">دائم</span><span class="sxs-lookup"><span data-stu-id="70f1f-605">Permanent</span></span>             | <span data-ttu-id="70f1f-606">دائم</span><span class="sxs-lookup"><span data-stu-id="70f1f-606">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="70f1f-607">الحالة الاجتماعية</span><span class="sxs-lookup"><span data-stu-id="70f1f-607">Marital status</span></span>

<span data-ttu-id="70f1f-608">يتم تعيين قيم الحالة الاجتماعية إلى Dayforce وترجمتها، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="70f1f-608">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="70f1f-609">يعرض الجدول التالي كيفية تعيين قيم الحالة الاجتماعية إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="70f1f-609">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="70f1f-610">Talent</span><span class="sxs-lookup"><span data-stu-id="70f1f-610">Talent</span></span>                 | <span data-ttu-id="70f1f-611">Dayforce</span><span class="sxs-lookup"><span data-stu-id="70f1f-611">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="70f1f-612">متزوج</span><span class="sxs-lookup"><span data-stu-id="70f1f-612">Married</span></span>                | <span data-ttu-id="70f1f-613">متزوج</span><span class="sxs-lookup"><span data-stu-id="70f1f-613">Married</span></span>                   |
| <span data-ttu-id="70f1f-614">واحد</span><span class="sxs-lookup"><span data-stu-id="70f1f-614">Single</span></span>                 | <span data-ttu-id="70f1f-615">واحد</span><span class="sxs-lookup"><span data-stu-id="70f1f-615">Single</span></span>                    |
| <span data-ttu-id="70f1f-616">أرمل</span><span class="sxs-lookup"><span data-stu-id="70f1f-616">Widowed</span></span>                | <span data-ttu-id="70f1f-617">أرمل</span><span class="sxs-lookup"><span data-stu-id="70f1f-617">Widowed</span></span>                   |
| <span data-ttu-id="70f1f-618">مطلق</span><span class="sxs-lookup"><span data-stu-id="70f1f-618">Divorced</span></span>               | <span data-ttu-id="70f1f-619">مطلق</span><span class="sxs-lookup"><span data-stu-id="70f1f-619">Divorced</span></span>                  |
| <span data-ttu-id="70f1f-620">شراكة مسجلة</span><span class="sxs-lookup"><span data-stu-id="70f1f-620">Registered Partnership</span></span> | <span data-ttu-id="70f1f-621">الشراكة المحلية</span><span class="sxs-lookup"><span data-stu-id="70f1f-621">Domestic Partnership</span></span>      |
| <span data-ttu-id="70f1f-622">بلا</span><span class="sxs-lookup"><span data-stu-id="70f1f-622">None</span></span>                   | <span data-ttu-id="70f1f-623">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="70f1f-623">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="70f1f-624">تعايش</span><span class="sxs-lookup"><span data-stu-id="70f1f-624">Cohabiting</span></span>             | <span data-ttu-id="70f1f-625">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="70f1f-625">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="70f1f-626">الجنس</span><span class="sxs-lookup"><span data-stu-id="70f1f-626">Gender</span></span>

<span data-ttu-id="70f1f-627">يتم تعيين الجنس إلى Dayforce وترجمته، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="70f1f-627">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="70f1f-628">يعرض الجدول التالي كيفية تعيين الجنس إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="70f1f-628">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="70f1f-629">Talent</span><span class="sxs-lookup"><span data-stu-id="70f1f-629">Talent</span></span>       | <span data-ttu-id="70f1f-630">Dayforce</span><span class="sxs-lookup"><span data-stu-id="70f1f-630">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="70f1f-631">ذكر</span><span class="sxs-lookup"><span data-stu-id="70f1f-631">Male</span></span>         | <span data-ttu-id="70f1f-632">ذكر</span><span class="sxs-lookup"><span data-stu-id="70f1f-632">Male</span></span>                      |
| <span data-ttu-id="70f1f-633">أنثى</span><span class="sxs-lookup"><span data-stu-id="70f1f-633">Female</span></span>       | <span data-ttu-id="70f1f-634">أنثى</span><span class="sxs-lookup"><span data-stu-id="70f1f-634">Female</span></span>                    |
| <span data-ttu-id="70f1f-635">غير محدد</span><span class="sxs-lookup"><span data-stu-id="70f1f-635">Non-specific</span></span> | <span data-ttu-id="70f1f-636">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="70f1f-636">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="70f1f-637">أسلوب الدفع</span><span class="sxs-lookup"><span data-stu-id="70f1f-637">Payment method</span></span>

<span data-ttu-id="70f1f-638">تقدم طرق دفع للموظف والشركة طريقة لوصف كيفية تسديد مرتبات وأجور الموظفين.</span><span class="sxs-lookup"><span data-stu-id="70f1f-638">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="70f1f-639">يتم تعيين طرق الدفع إلى Dayforce وترجمتها، حسب الحاجة، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="70f1f-639">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="70f1f-640">يعرض الجدول التالي كيفية تعيين طرق الدفع إلى Dayforce.</span><span class="sxs-lookup"><span data-stu-id="70f1f-640">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="70f1f-641">Talent</span><span class="sxs-lookup"><span data-stu-id="70f1f-641">Talent</span></span>             | <span data-ttu-id="70f1f-642">Dayforce</span><span class="sxs-lookup"><span data-stu-id="70f1f-642">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="70f1f-643">نقدي</span><span class="sxs-lookup"><span data-stu-id="70f1f-643">Cash</span></span>               | <span data-ttu-id="70f1f-644">نقدي</span><span class="sxs-lookup"><span data-stu-id="70f1f-644">Cash</span></span>                      |
| <span data-ttu-id="70f1f-645">دفع إلكتروني</span><span class="sxs-lookup"><span data-stu-id="70f1f-645">Electronic Payment</span></span> | <span data-ttu-id="70f1f-646">التحويل</span><span class="sxs-lookup"><span data-stu-id="70f1f-646">Transfer</span></span>                  |
| <span data-ttu-id="70f1f-647">فحص</span><span class="sxs-lookup"><span data-stu-id="70f1f-647">Check</span></span>              | <span data-ttu-id="70f1f-648">شيك</span><span class="sxs-lookup"><span data-stu-id="70f1f-648">Cheque</span></span>                    |
| <span data-ttu-id="70f1f-649">حوالة مصرفية</span><span class="sxs-lookup"><span data-stu-id="70f1f-649">Bank Draft</span></span>         | <span data-ttu-id="70f1f-650">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="70f1f-650">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="70f1f-651">‏‏غير ذلك</span><span class="sxs-lookup"><span data-stu-id="70f1f-651">Other</span></span>              | <span data-ttu-id="70f1f-652">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="70f1f-652">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="70f1f-653">نوع الحساب البنكي</span><span class="sxs-lookup"><span data-stu-id="70f1f-653">Bank account type</span></span>

<span data-ttu-id="70f1f-654">يتم استخدام أنواع الحسابات البنكية للدفع الإلكتروني للموظفين.</span><span class="sxs-lookup"><span data-stu-id="70f1f-654">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="70f1f-655">يتم تعيين أنواع الحسابات البنكية إلى Dayforce كمعلومات حساب التحويل.</span><span class="sxs-lookup"><span data-stu-id="70f1f-655">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="70f1f-656">وتتم ترجمة أنواع الحسابات البنكية، كما هو مناسب، إلى القيم المقبولة عند التكامل.</span><span class="sxs-lookup"><span data-stu-id="70f1f-656">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="70f1f-657">Talent</span><span class="sxs-lookup"><span data-stu-id="70f1f-657">Talent</span></span>            | <span data-ttu-id="70f1f-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="70f1f-658">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="70f1f-659">حساب شيكات</span><span class="sxs-lookup"><span data-stu-id="70f1f-659">Checking Account</span></span>  | <span data-ttu-id="70f1f-660">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="70f1f-660">CheckingAccount</span></span>           |
| <span data-ttu-id="70f1f-661">حساب الراتب</span><span class="sxs-lookup"><span data-stu-id="70f1f-661">Payroll Account</span></span>   | <span data-ttu-id="70f1f-662">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="70f1f-662">PayrollAccount</span></span>            |
| <span data-ttu-id="70f1f-663">حساب توفير</span><span class="sxs-lookup"><span data-stu-id="70f1f-663">Savings Account</span></span>   | <span data-ttu-id="70f1f-664">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="70f1f-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="70f1f-665">حساب BankGirot</span><span class="sxs-lookup"><span data-stu-id="70f1f-665">BankGirot account</span></span> | <span data-ttu-id="70f1f-666">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="70f1f-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="70f1f-667">حساب PlusGirot</span><span class="sxs-lookup"><span data-stu-id="70f1f-667">PlusGirot account</span></span> | <span data-ttu-id="70f1f-668">*غير مدعوم بواسطة المكسيك*</span><span class="sxs-lookup"><span data-stu-id="70f1f-668">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="70f1f-669">أكواد الأرباح</span><span class="sxs-lookup"><span data-stu-id="70f1f-669">Earning codes</span></span>

<span data-ttu-id="70f1f-670">تحدد أكواد الأرباح بشكل فريد كل نوع من أنواع الأرباح التي يحصل عليها العاملون.</span><span class="sxs-lookup"><span data-stu-id="70f1f-670">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="70f1f-671">تغطي الأكواد معلمات متنوعة ترتبط بالأرباح، مثل قواعد المحاسبة وقوانين الضرائب ومتطلبات إعداد التقارير وقدرات المبلغ الإجمالي.</span><span class="sxs-lookup"><span data-stu-id="70f1f-671">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="70f1f-672">إذا تم استخدام تكرار غير معتمد، يُستخدم التكرار **كل عملية دفع** بشكل افتراضي للحساب.</span><span class="sxs-lookup"><span data-stu-id="70f1f-672">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="70f1f-673">التكرارات المدعومة</span><span class="sxs-lookup"><span data-stu-id="70f1f-673">Supported frequencies</span></span>

- <span data-ttu-id="70f1f-674">الكل</span><span class="sxs-lookup"><span data-stu-id="70f1f-674">All</span></span>
- <span data-ttu-id="70f1f-675">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="70f1f-675">EVERYPAY</span></span>
- <span data-ttu-id="70f1f-676">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="70f1f-676">EACHPAYPERIOD</span></span>
- <span data-ttu-id="70f1f-677">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="70f1f-677">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="70f1f-678">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="70f1f-678">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="70f1f-679">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-679">1OFMTH</span></span>
- <span data-ttu-id="70f1f-680">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-680">LASTOFMTH</span></span>
- <span data-ttu-id="70f1f-681">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-681">2OFMTH</span></span>
- <span data-ttu-id="70f1f-682">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-682">3OFMTH</span></span>
- <span data-ttu-id="70f1f-683">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-683">4OFMTH</span></span>
- <span data-ttu-id="70f1f-684">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-684">5OFMTH</span></span>
- <span data-ttu-id="70f1f-685">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-685">1N2OFMTH</span></span>
- <span data-ttu-id="70f1f-686">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-686">3N4OFMTH</span></span>
- <span data-ttu-id="70f1f-687">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-687">1N3OFMTH</span></span>
- <span data-ttu-id="70f1f-688">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-688">1N4OFMTH</span></span>
- <span data-ttu-id="70f1f-689">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-689">2N3OFMTH</span></span>
- <span data-ttu-id="70f1f-690">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-690">2N4OFMTH</span></span>
- <span data-ttu-id="70f1f-691">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-691">1N2N3OFMTH</span></span>
- <span data-ttu-id="70f1f-692">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-692">1N2N4OFMTH</span></span>
- <span data-ttu-id="70f1f-693">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-693">1N3N4OFMTH</span></span>
- <span data-ttu-id="70f1f-694">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-694">2N3N4OFMTH</span></span>
- <span data-ttu-id="70f1f-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="70f1f-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="70f1f-696">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="70f1f-696">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="70f1f-697">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="70f1f-697">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="70f1f-698">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="70f1f-698">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="70f1f-699">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="70f1f-699">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="70f1f-700">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="70f1f-700">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="70f1f-701">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="70f1f-701">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="70f1f-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="70f1f-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="70f1f-703">العناوين</span><span class="sxs-lookup"><span data-stu-id="70f1f-703">Addresses</span></span>

<span data-ttu-id="70f1f-704">يتطلب تعريف أكواد بلد أو منطقة وولاية وإقليم (بلدية) معينة تنسيقات معينة تستطيع Dayforce والموفرين في البلد/في المنطقة التعرف عليها.</span><span class="sxs-lookup"><span data-stu-id="70f1f-704">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="70f1f-705">على الرغم من أن تنسيق المدن يعتبر مرنًا، يجب أن تكون كل مدينة مقترنة بولاية.</span><span class="sxs-lookup"><span data-stu-id="70f1f-705">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="70f1f-706">Talent</span><span class="sxs-lookup"><span data-stu-id="70f1f-706">Talent</span></span>              | <span data-ttu-id="70f1f-707">Dayforce</span><span class="sxs-lookup"><span data-stu-id="70f1f-707">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="70f1f-708">البلد/المنطقة</span><span class="sxs-lookup"><span data-stu-id="70f1f-708">Country/Region</span></span>      | <span data-ttu-id="70f1f-709">كود البلد</span><span class="sxs-lookup"><span data-stu-id="70f1f-709">Country Code</span></span>          |
| <span data-ttu-id="70f1f-710">الرمز البريدي</span><span class="sxs-lookup"><span data-stu-id="70f1f-710">Zip/Postal Code</span></span>     | <span data-ttu-id="70f1f-711">الرمز البريدي</span><span class="sxs-lookup"><span data-stu-id="70f1f-711">Postal Code</span></span>           |
| <span data-ttu-id="70f1f-712">المنطقة‬</span><span class="sxs-lookup"><span data-stu-id="70f1f-712">State</span></span>               | <span data-ttu-id="70f1f-713">كود الولاية</span><span class="sxs-lookup"><span data-stu-id="70f1f-713">State Code</span></span>            |
| <span data-ttu-id="70f1f-714">المدينة</span><span class="sxs-lookup"><span data-stu-id="70f1f-714">City</span></span>                | <span data-ttu-id="70f1f-715">المدينة</span><span class="sxs-lookup"><span data-stu-id="70f1f-715">City</span></span>                  |
| <span data-ttu-id="70f1f-716">الإقليم</span><span class="sxs-lookup"><span data-stu-id="70f1f-716">County</span></span>              | <span data-ttu-id="70f1f-717">المقاطعة (بلدية)</span><span class="sxs-lookup"><span data-stu-id="70f1f-717">County (Municipality)</span></span> |
| <span data-ttu-id="70f1f-718">الشارع</span><span class="sxs-lookup"><span data-stu-id="70f1f-718">Street</span></span>              | <span data-ttu-id="70f1f-719">سطر العنوان 1</span><span class="sxs-lookup"><span data-stu-id="70f1f-719">Address Line 1</span></span>        |
| <span data-ttu-id="70f1f-720">رقم الشارع</span><span class="sxs-lookup"><span data-stu-id="70f1f-720">Street Number</span></span>       | <span data-ttu-id="70f1f-721">سطر العنوان 2</span><span class="sxs-lookup"><span data-stu-id="70f1f-721">Address Line 2</span></span>        |
| <span data-ttu-id="70f1f-722">ملحق المبنى</span><span class="sxs-lookup"><span data-stu-id="70f1f-722">Building Complement</span></span> | <span data-ttu-id="70f1f-723">سطر العنوان 5</span><span class="sxs-lookup"><span data-stu-id="70f1f-723">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="70f1f-724">رقم جواز السفر</span><span class="sxs-lookup"><span data-stu-id="70f1f-724">Passport number</span></span>

<span data-ttu-id="70f1f-725">بإمكان الموظفين إعلان معلومات جواز السفر.</span><span class="sxs-lookup"><span data-stu-id="70f1f-725">Employees can declare passport information.</span></span> <span data-ttu-id="70f1f-726">هذه المعلومات هي نوع من أنواع تعريف **جواز السفر** وهي تتكامل في Dayforce كجزء من معلومات الموظف خاصة بالمكسيك.</span><span class="sxs-lookup"><span data-stu-id="70f1f-726">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="70f1f-727">نوع التعريف = "جواز سفر"</span><span class="sxs-lookup"><span data-stu-id="70f1f-727">Identification Type = "Passport"</span></span>
- <span data-ttu-id="70f1f-728">تاريخ الإصدار</span><span class="sxs-lookup"><span data-stu-id="70f1f-728">Issued Date</span></span>
- <span data-ttu-id="70f1f-729">تاريخ انتهاء الصلاحية</span><span class="sxs-lookup"><span data-stu-id="70f1f-729">Expiration Date</span></span>

<span data-ttu-id="70f1f-730">بإمكان الموظفين الإعلان عن أرقام تعريف متعددة من نوع التعريف **جواز سفر**.</span><span class="sxs-lookup"><span data-stu-id="70f1f-730">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="70f1f-731">ومع ذلك، يتم دمج إدخال جواز السفر النشط الحالي فقط في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="70f1f-731">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="70f1f-732">إذا انتهت صلاحية جميع إدخالات جوازات السفر، فسيتكامل جواز السفر الذي تم إصداره مؤخرًا في Dayforce.</span><span class="sxs-lookup"><span data-stu-id="70f1f-732">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
